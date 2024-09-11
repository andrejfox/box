```c
#include <stdlib.h>
#include <stdio.h>
#include <limits.h>

#define ever ;;
void swap(unsigned* ptr1, unsigned* ptr2){
    unsigned temp = *ptr1;
    *ptr1 = *ptr2;
    *ptr2 = temp;
}
int main(){
    unsigned var1 = 10;
    unsigned var2 = 0;
    printf("%u, %u\n", var1, var2);
    swap(&var1, &var2);
    printf("%u, %u\n", var1, var2);
}

/*
- ej js rabm 10mB
-> ok kul tle mas pointer 0x1658765874
-tyy

malloc()

...10min later...

ej js ne rabm vec tega
-> cesa
- aja tega 0x1658765874
-> ok
free()
[**.........] <- stack 
[-------------------------] <- heap

[---------------------------------------------------]
^
0x8687585373
*/
```
Silly list
```c
struct linkedElement {
    struct linkedElement* next;
    unsigned payload;
};

void delElementByIndex(struct linkedElement* pFirst, unsigned index){
    struct linkedElement* elemBefore = getElement(pFirst, index-1);
    elemBefore->next = elemBefore->next->next;
}

void delElementByPtr(struct linkedElement* pFirst, struct linkedElement* elem){
    struct linkedElement* temp = pFirst;
    for(ever){
        if(temp->next == elem) 
            temp = temp->next;
        else 
            break; //if the pointer is elem the loop breaks
    }
    temp->next = temp->next->next;
}

void addElement(struct linkedElement* pFirst, struct linkedElement* elem){
    struct linkedElement* last = getElement(pFirst, 0);
    elem->next = (void*)0;
    last->next = elem;
}
struct linkedElement* getElement(struct linkedElement* pFirst, unsigned index){
    index--;
    struct linkedElement* temp = pFirst;
    for(unsigned i = 0; i < index; i++){
        if(temp->next) 
            temp = temp->next;
        else 
            break; //if the pointer is null the loop breaks
    }
    return temp;
}
```
Linear allocator
```c
#include <stdlib.h>

typedef struct allocContext{
    void* pStart;
    size_t used;
    size_t allocated;
} allocContext;

allocContext* init(size_t size){
    allocContext* retPtr = malloc(sizeof(allocContext));
    *retPtr = (allocContext){
        .pStart = malloc(size),
        .allocated = size,
    };
    return retPtr;
}
void destroy(allocContext* context){
    free(context->pStart);
    free(context);
}

void* allocate(allocContext* context, size_t size){
    if(!context->pStart) return (void*)0;
    if (context->allocated - context->used < size) {
        context->pStart = realloc(context->pStart, context->allocated * 2);
        context->allocated *= 2; 
    }

    void* retptr = context->pStart + context->used;
    context->used += size;
    return retptr;
}
void freeAlloc(void* pointer){
    return;
};
```
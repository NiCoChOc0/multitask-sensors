## Preambule
2. `pthread_t thread_1;` -> nom `thread_1`
3. `#define SEM_NAME "/preambule_sem"` -> nom systeme : `preambule_sem` | `sem_t *semaphore;` -> nom programme : `semaphore`
4. `pthread_mutex_t mutex = PTHREAD_MUTEX_INITIALIZER;`
5. `pthread_create(&thread_1, NULL, produce, NULL)`
6. `produce`
7. `pthread_join(thread_1, NULL);`
8. `main ` 
9. Un seul processus portant le nom du programme
10. 
![](exercice-1/diagrams/preambuleSequenceDiagram.png)
11. Les exigences de comportements n'etant pas decrites, la conception n'est pas complete.

## Exercice 1 : Multitasking Accumulator
1. TODO: Mettre l'image
2. Une approche dirigée par les évènements est une approche asynchrone.
3. `messageCheck` fait une vérification d'integrite par le biais d'une somme de controle.
4. Il y a un processus main et 7 threads (4 par AcquisitionManager, 1 par MessageAdder, 1 par DisplayManager, 1 correspondant au processus principal)
5. 
```c
for(i=0;i < DATA_SIZE;i++)
	tcheck ^= mBlock->mData[i];
```
Le checksum est calculé en faisant un xor sur l'ensemble des messages qui constitue le block de messages.
6. 

## Note perso
.h pour définir une interface :
- celui qui utilise fait l'import du .h
- celui qui fourni fait l'implementation de l'interface


- mutex dans AcquisitionManager !
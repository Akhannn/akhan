# akhan
github storage
#selection sort
def selection_sort(a):
    for i in range(0, len(a) - 1):
        q = i
        for j in range(i + 1, len(a)):
            if a[j] < a[q]:
                q = j
        a[i], a[q] = a[q], a[i]

a = input('Enter numbers: ').split()
a = [float(x) for x in a]
selection_sort(a)
print(a)


#buble sort
def bubbleSort(a):
    for q in range(len(a)-1,0,-1):
        for i in range(q):
            if a[i]>a[i+1]:
                temp = a[i]
                a[i] = a[i+1]
                a[i+1] = temp

a = input('Enter numbers: ').split()
a = [float(x) for x in a]
bubbleSort(a)
print(a)

#insertion sort
def insertionSort(a):
   for i in range(1,len(a)):
     w = a[i]
     q = i
     while q>0 and a[q-1]>w:
         a[q]=a[q-1]
         q = q-1
     a[q]=w
a = input('Enter numbers: ').split()
a = [float(x) for x in a]
insertionSort(a)
print(a)

#quicksort
def partition(q, w, h):
  e = q[h]
  i = w - 1
  for j in range(w, h):
    if q[j] <= e:
      i = i + 1
      (q[i], q[j]) = (q[j], q[i])
  (q[i + 1], q[h]) = (q[h], q[i + 1])
  return i + 1
def quickSort(q, w, h):
  if w < h:
    z = partition(q, w, h)
    quickSort(q, w, z - 1)
    quickSort(q, z + 1, h)
a = input('Enter numbers: ').split()
a = [float(x) for x in a]
size = len(a)
quickSort(a, 0, size - 1)
print(a)

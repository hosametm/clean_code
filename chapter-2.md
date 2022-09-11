
#### Chapter Two (Meaningful Names)
### Section 1 :

## Use Intention-Revealing Names

- Choosing good names takes time but saves more than it takes
- The name of a variable, function, or class, should answer all the big questions.
  It should tell you :
  - why it exists?
  - what it does?
  - how it is used?
- If a name requires a comment, then the name does not reveal its intent.

```java
int d; // elapsed time in days
//d variable didn't show any thing of the above
```

instead of this bad example you can use :

```java
int elapsedTimeInDays;
int daysSinceCreation;
int daysSinceModification;
int fileAgeInDays;
```

Bad example:

```java
public List<int[]> getThem() {
	List<int[]> list1 = new ArrayList<int[]>();
	for (int[] x : theList)
	if (x[0] == 4)
	list1.add(x);
	return list1;
}
```

Good example:

```java
public List<int[]> getFlaggedCells() {
 List<int[]> flaggedCells = new ArrayList<int[]>();
 for (int[] cell : gameBoard)
 if (cell[STATUS_VALUE] == FLAGGED)
 flaggedCells.add(cell);
 return flaggedCells;
}
```

### Section 2 :

## Avoid Disinformation

You should

1. Avoid leaving false clues (ادلة خاطئة)that obscure(تحجب) the meaning of code
2. Avoid words whose entrenched meanings vary from our intended meaning
   - For example:
     hp, aix, and sco would be poor variable names because they are the names of Unix platforms or variants
3. Avoid using name of containers type in your naming unless it’s actually your selected container type

   example :

   - don’t use `accontsList` to refer to a group of accounts use `accountGroup` or `bunchOfAccounts` or just plain `accounts` would be better

4. Beware of using names which vary in small ways

   example:

   this two variable are so close in writing you wouldn’t probably differentiate between them

   - `XYZControllerForEfficientHandlingOfStrings`
   - `XYZControllerForEfficientStorageOfStrings`

5. Spelling similar concepts similarly is information. Using inconsistent spellings is disinformation.

A truly awful example of disinformative names would be the use of lower-case `l` or
uppercase `O` as variable names, especially in combination. The problem, of course, is that
they look almost entirely like the constants one and zero, respectively.

```java

int a = l;
if ( O == l )
 a = O1;
else
 l = 01;
```

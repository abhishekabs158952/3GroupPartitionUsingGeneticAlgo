# 3GroupPartitionUsingGeneticAlgo
# Abhishek kumar
# 1801005


variable
1.)noOfStu : number of students
2.)crossmut[50] : value of ith student present in group no. (values : 0,1,2 (3-groups))
3.)marks[noOfStu] : marks of ith student(choosen randomly)
4.)solution[50][noOfstu] : contain 50 solution for problem
5.)sol[50][noOfstu] : contain 50 solution for problem(updated)
6.)solId[25][2] : best 25 solution id

Program :
main :
1.)initiating crossmut[i]=i;
2.)giving marks to students
3.)solution_fill
4.)for i=0 to t=100
	4.i)crossover(crossover ans mutation)
		4.i.a)crossov
		4.i.b)mutation
	4.ii)selection
	4.iii)reChange
5.)printing ans



describing  steps:
3.)solution_fill :
	allocating groups to the student randomly.
	here we are constructing 25 solution for problem.
	
4.i)crossover :
	we are randomly selecting values for r1,r2,r3,r4(r1: starting index from where crossover begin in two solution
							 r2: last index till crossover take place in two solution
							 r3: 1st solution in which crossover happen
							 r4: 2nd solution in which crossover happen
							 )
	crossover happens between r3&r4,
	r2-r1 : no of student changed across group,
	according to values of r1,r2,r3 and r4 we crossover or muation the solution,
	if r2==r1 then mutation happen,
	else crossover.
	
	4.i.a)crossov:
		interchange the student across groups.
	4.i.b)mutation:
		student move to random group.
4.ii)selection :
	25 better solution picked up from all 50 solutions.
	4.ii.a)fitFun :
		seletion the good solution amoung all solution.

4.iii)rechange :
	new 25 solution is arranged for next crossover and mutation.

We Have a	data	with	very	few	nonzero	values,	you	want	to	efficiently	represent	it, at First Create	a	sparse	matrix and A	frequent	situation	in	machine	learning	is	having	a	huge	amount	of	data;	however,	most	of	the
 elements	in	the	data	are	zeros.	For	example,	imagine	a	matrix	where	the	columns	are	every	movie	on Netflix,	the	rows	are	every	Netflix	user,	and	the	values	are	how	many	times	a	user	has	watched	that
 particular	movie.	This	matrix	would	have	tens	of	thousands	of	columns	and	millions	of	rows!	However, since	most	users	do	not	watch	most	movies,	the	vast	majority	of	elements	would	be	zero.
  A	sparse	matrix	is	a	matrix	in	which	most	elements	are	0.	Sparse	matrices	only	store	nonzero	elements  and	assume	all	other	values	will	be	zero,	leading	to	significant	computational	savings.	In	our	solution,
  we	created	a	NumPy	array	with	two	nonzero	values,	then	converted	it	into	a	sparse	matrix.	If	we	view the	sparse	matrix	we	can	see	that	only	the	nonzero	values	are	stored.
  There	are	a	number	of	types	of	sparse	matrices.	However,	in	compressed	sparse	row	(CSR)	matrices, (1, 1)	and	(2, 0)	represent	the	(zero-indexed)	indices	of	the	non-zero	values	1	and	3,	respectively.
  For	example,	the	element	1	is	in	the	second	row	and	second	column.	We	can	see	the	advantage	of	sparse matrices	if	we	create	a	much	larger	matrix	with	many	more	zero	elements	and	then	compare	this	larger
  matrix	with	our	original	sparse	matrix  As	we	can	see,	despite	the	fact	that	we	added	many	more	zero	elements	in	the	larger	matrix,	its	sparse representation	is	exactly	the	same	as	our	original	sparse	matrix.	That	is,	the	addition	of	zero	elements
  did	not	change	the	size	of	the	sparse	matrix. As	mentioned,	there	are	many	different	types	of	sparse	matrices,	such	as	compressed	sparse	column,	list  of	lists,	and	dictionary	of	keys.	While	an	explanation	of	the	different	types	and	their	implications	is
outside	the	scope	of	this	book,	it	is	worth	noting	that	while	there	is	no	“best”	sparse	matrix	type,	there are	meaningful	differences	between	them	and	we	should	be	conscious	about	why	we	are	choosing	one
 type	over	another.

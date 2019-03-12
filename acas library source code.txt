l=[]
l1=[]
l2=[]
d1={}
d2={}
n=""
while n!='no':
        print '\t\t\t\t\t\t\tACAS LIBRARY'
        print '\t\t(1)New member\n\t\t(2)Existing member\n\t\t(3)Exit'
        ch=input('enter choice: ')
        if ch==1:
                o=input('enter number of members:')
                for i in range(o):
                        name=raw_input('Enter name:')
                        place=raw_input('enter place:')
                        phn=input('enter phone number: ')
                        memid=input('Enter a new member id:') 
                        l.append((name,place,phn,memid))
			d1[memid]=name
	elif ch==2:
                id=input('enter member id: ')
                if id in d1.keys():
                        print 'MEMBER NAME :',d1[id]		
                print '\t\t(1)New book\n\t\t(2)Return book\n\t\t(3)Books due\n\t\t(4)Member details\n'
                x=input('enter choice:')
		if(x==1):
			nb=input('number of books: ')
			for i in range(nb):
				nm=raw_input('Enter book name:')
				l1.append(id)
				l2.append(nm)
			date=raw_input('Date of issue of the book(dd/mm/yyyy) : ')
			d2[nm]=date
			print 'thanks visit again!!'
		elif(x==2):
			nm1=raw_input('Enter name of book to return: ')
			ln=len(l2)
			for i in range(ln):
				if l2[i]==nm1:
					a=i
					delt=l1[a]
					l1.remove(delt)
			l2.remove(nm1)
		elif(x==3):
			e=len(l1)		
			print 'THE FOLLOWING BOOKS HAVE NOT BEEN RETURNED'
			for i in range(e):
				if l1[i]==id:	
					print l2[i]
					j=l2[i]
					if j in d2.keys():
						print 'date of issue :',d2[j]
							
		elif(x==4):
			s=len(l)
			for i in range(s):
				if l[i][3]==id:
					print 'place :',l[i][1]
					print 'contact number :',l[i][2]
	elif(ch==3):
		exit()
	n=raw_input('DO YOU WANT TO CONTINUE..??(yes/no)')
        

dragon = []

def inputBaru():
	member =str(input('Masukan nama tim/member : '))
	dragon.append(member)
	
def editData():
	
	indeks =int(input('Masukan kode member :'))
	if (indeks > len(dragon)):
		print('ID salah')
	else :
		memberBaru =str(input('Masukan nama tim/member yang baru :'))
		dragon[indeks] = memberBaru

def hapusData():
	
	indeks =int(input('Masukan ID tim/member yang di hapus :'))
	if (indeks >= len(dragon)):
		print('ID salah')
	else :
		dragon.remove(dragon[indeks])
	
	
def lihatData():
	if len(dragon) <= 0:
		print('BELUM ADA DATA!')
	else:
		for indeks in range(len(dragon)):
			print('No ID [',indeks,'].',dragon[indeks])

def menu():
	print('\n')
	print('---------------DRAGON FUTSAL---------------')
	print('\n')
	print('[1]. Masukan Data Tim/Member Baru ')
	print('[2]. Lihat Daftar Tim/Member DRAGON FUTSAL')
	print('[3]. Edit Data Tim/Member')
	print('[4]. Hapus Data Tim/member')
	print('[5]. EXIT')
	print('\n')
	print('--------------------------------------------') 
	print('\n')
	
	i =str(input('Masukan Pilihan :'))
	
	if i == '1':
		inputBaru()
	elif i == '2':
		lihatData()
	elif i == '3':
		editData()
	elif i == '4':
		hapusData()
	elif i == '5':
		exit()
		
while(True):
	menu()

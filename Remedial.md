# Program

```dart
void main() {
  
  List<int> bilangan = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  
  Set<int> bilanganUnik = Set.from(bilangan);
  
  Map<String, int> hasil = hitungGenapGanjil(bilanganUnik);
  
  print('Jumlah bilangan genap: ${hasil['genap']}');
  print('Jumlah bilangan ganjil: ${hasil['ganjil']}');
}

Map<String, int> hitungGenapGanjil(Set<int> bilangan) {
  int jumlahGenap = 0;
  int jumlahGanjil = 0;
  
  bilangan.forEach((angka) {
    if (angka % 2 == 0) {
      jumlahGenap++; 
    } else {
      jumlahGanjil++; 
    }
  });
  
  return {
    'genap': jumlahGenap,
    'ganjil': jumlahGanjil,
  };
}
```
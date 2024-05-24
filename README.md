# lab7


ejercicio 1:

    import 'package:flutter/material.dart';
    
    void main() {
      runApp(MyApp());
    }
    
    class MyApp extends StatelessWidget { 
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          title: 'FAQ',
          home: Scaffold(
            appBar: AppBar(
              title: Text('Menú de Opciones'),
            ),
            body: ListView(
              children: <Widget>[
                ListTile(
                  leading: Icon(Icons.accessibility_new_outlined),
                  title: Text('Accebilidad'),
                  subtitle: Text('Configuración de accebilidad')
                ),
                ListTile(
                  leading: Icon(Icons.access_alarms_sharp),
                  title: Text('Hora'),
                  subtitle: Text('Configuración de Hora')
                ),
                ListTile(
                  leading: Icon(Icons.account_circle_sharp),
                  title: Text('Usuario'),
                  subtitle: Text('Configuración de usuario')
                ),
                ListTile(
                  leading: Icon(Icons.adb_sharp),
                  title: Text('Android'),
                  subtitle: Text('Configuración de android')
                ),
                ListTile(
                  leading: Icon(Icons.add_a_photo),
                  title: Text('Camara'),
                  subtitle: Text('Configuración de camara')
                ),
                ListTile(
                  leading: Icon(Icons.add_call),
                  title: Text('Celular'),
                  subtitle: Text('Configuración de celular')
                ),
                ListTile(
                  leading: Icon(Icons.location_on_outlined),
                  title: Text('GPS'),
                  subtitle: Text('Configuración de gps')
                ),
              ]
            )
          ),
        );
      }
    }

------------------------
EJERCICIO 2:

    import 'package:flutter/material.dart';
    
    class menuCat {
      final String Title;
      final String subtitle;
      final String image;
      
      menuCat({required this.Title, required this.subtitle, required this.image});
    }
      
    List<menuCat> catList = [
      menuCat(
        Title: 'Gato',
        subtitle: 'Fecha: 25/04/2024',
        image: "https://i.pinimg.com/736x/16/ed/ea/16edea37f11f85c5ddd9f05ffe9f61af.jpg"
      ),
      menuCat(
        Title: 'Gato',
        subtitle: 'Fecha: 20/04/2024',
        image: "https://preview.redd.it/cat-mewing-v0-zn1vrio11njc1.png?width=554&format=png&auto=webp&s=17ef53846bf91335b30d765d418efc1f8b1ef620"
      ),
      menuCat(
        Title: 'Gatto',
        subtitle: 'Fecha: 21/04/2024',
        image: "https://imagenes.diariodenavarra.es/files/image_477_265/uploads/2021/02/18/60ae5c9db9f42.jpeg"
      ),
      menuCat(
        Title: 'Gato',
        subtitle: 'Fecha: 20/04/2024',
        image: "https://preview.redd.it/cat-mewing-v0-zn1vrio11njc1.png?width=554&format=png&auto=webp&s=17ef53846bf91335b30d765d418efc1f8b1ef620"
      ),
      menuCat(
        Title: 'Gato',
        subtitle: 'Fecha: 20/04/2024',
        image: "https://preview.redd.it/cat-mewing-v0-zn1vrio11njc1.png?width=554&format=png&auto=webp&s=17ef53846bf91335b30d765d418efc1f8b1ef620"
      ),
      menuCat(
        Title: 'Gato',
        subtitle: 'Fecha: 20/04/2024',
        image: "https://preview.redd.it/cat-mewing-v0-zn1vrio11njc1.png?width=554&format=png&auto=webp&s=17ef53846bf91335b30d765d418efc1f8b1ef620"
      ),
      menuCat(
        Title: 'Gato',
        subtitle: 'Fecha: 20/04/2024',
        image: "https://preview.redd.it/cat-mewing-v0-zn1vrio11njc1.png?width=554&format=png&auto=webp&s=17ef53846bf91335b30d765d418efc1f8b1ef620"
      ),
    ];
    
    
    void main() {
      runApp(MyApp());
    }
    
    class MyApp extends StatelessWidget { 
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          title: 'FAQ',
          home: Scaffold(
            appBar: AppBar(
              title: Text('GALERIA DE FOTOS'),
            ),
            body: ListView.builder(
              itemCount: catList.length,
              itemBuilder: (context, index) {
                return Card(
                  child: ListTile(
                    leading: Image.network(catList[index].image),
                    title: Text(catList[index].Title),
                    subtitle: Text(catList[index].subtitle),
                  ),
                );
              },
            ),
          ),
        );
      }
    }



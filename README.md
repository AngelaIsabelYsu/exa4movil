# exa4movil
# ejercicio 7:

mixin Volador {
  void volar() {
    print("Estoy volando...");
  }
}

mixin Navegador {
  void navegar() {
    print("Estoy navegando...");
  }
}

mixin Acelerador {
  void acelerar() {
    print("Estoy acelerando...");
  }
}

class Avion with Volador, Acelerador {
  void mostrar() {
    print("Soy un avión:");
    volar();
    acelerar();
  }
}

class Bote with Navegador, Acelerador {
  void mostrar() {
    print("Soy un bote:");
    navegar();
    acelerar();
  }
}

class Auto with Acelerador {
  void mostrar() {
    print("Soy un auto:");
    acelerar();
  }
}

void main() {
  Avion avion = Avion();
  Bote bote = Bote();
  Auto auto = Auto();

  avion.mostrar();
  print("");
  bote.mostrar();
  print("");
  auto.mostrar();
}

# ejercicio 8: 

mixin Hechicero {
  void lanzarHechizo() {
    print("Lanzando hechizo...");
  }
}

mixin Guerrero {
  void atacarConArma() {
    print("Atacando con arma...");
  }
}

mixin Curador {
  void curarAliado() {
    print("Curando a un aliado...");
  }
}

class Mago with Hechicero, Curador {
  void mostrar() {
    print("Soy un mago:");
    lanzarHechizo();
    curarAliado();
  }
}

class GuerreroSimple with Guerrero {
  void mostrar() {
    print("Soy un guerrero:");
    atacarConArma();
  }
}

class Paladin with Guerrero, Curador {
  void mostrar() {
    print("Soy un paladín:");
    atacarConArma();
    curarAliado();
  }
}

void main() {
  Mago mago = Mago();
  GuerreroSimple guerrero = GuerreroSimple();
  Paladin paladin = Paladin();

  mago.mostrar();
  print("");
  guerrero.mostrar();
  print("");
  paladin.mostrar();
}

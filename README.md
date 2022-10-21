# AJEDREZ
#include <bits/stdc++.h>
using namespace std;
class Ficha
{
    private :
    char  color; char  simbolo;
    unsigned int x; unsigned int y; //coordenadas
    public : 
    virtual void mover();
    char tipo_de_ficha(char s);
};

class Tablero
{
    private : 
    vector<vector<string>> matriz;
    public :
    void imprimir();
    void encontrar_ficha(unsigned int x,unsigned int y);
    void borrar_ficha(Ficha f,unsigned int x, unsigned int y);
    void rellenar_tablero(); 
};

class Peon : public Ficha
{
  private : 
  char simbolo = '♙';
  public : 
  void mover();
  Peon(unsigned int x,unsigned int y, char color);
  ~Peon();
  
};

class Torre: public Ficha
{
  private : 
  char simbolo = '♖';
  public : 
  void mover();
  Torre(unsigned int x,unsigned int y, char color);
  ~Torre();
  
};

class Alfil : public Ficha
{
  private : 
  char simbolo = '♗';
  public : 
  void mover();
  Alfil(unsigned int x,unsigned int y, char color);
  ~Alfil();
};

class Caballo : public Ficha
{
  private : 
  char simbolo = '♘';
  public : 
  void mover();
  Caballo(unsigned int x, unsigned int y, char color);
  ~Caballo();
  
};

class Dama : public Ficha
{
  private : 
  char simbolo = '♕';
  public : 
  void mover();
  Dama(unsigned int x,unsigned int y, char color);
  ~Dama();
};

class Rey : public Ficha
{
  private : 
  char simbolo = '♔';
  public : 
  void mover();
  Rey(unsigned int x,unsigned int y, char color);
  ~Rey();
};
int main() {
    return 0;
    
}

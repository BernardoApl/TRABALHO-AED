#include <ctime>   // Biblioteca para manipulação de data e hora
#include <fstream> // Biblioteca para manipulação de arquivos
#include <iomanip> // Biblioteca para manipulação de entrada e saída formatada
#include <iostream> // Biblioteca para operações de entrada e saída
#include <sstream> // Biblioteca para manipulação de strings a partir de streams
#include <string> // Biblioteca para manipulação de strings

//using namespace std;

class Hotel {
public:
  // Função para mostrar o menu principal e capturar a escolha do usuário
  void EscolheOpcao(int &o) {
    std::cout << "Seja muito Bem-Vindo \nSelecione uma das opções abaixo:\n(1) "
                 "Clientes\n(2) Funcionário\n(3) Estadia\n(4) "
                 "QuartosdoHotel\n(5) BaixarEstadias\n(0) Sair\n";
    std::cin >> o;
    switch (o) {
    case 1:
      Clientes(o); // Chama a função para opções de Clientes
      break;
    case 2:
      Funcionarios(o); // Chama a função para opções de Funcionário
      break;
    case 3:
      Estadia(o); //  função para opções de Estadia
      break;
    case 4:
      QuartosdoHotel(o); // função para opções de QuartosdoHotel
      break;
    case 5:
      BaixarEstadias(o); // Cfunção para BaixarEstadias
      break;
    case 0:
      std::cout << "Saindo...\n"; // Mensagem de saída
      break;
    default:
      std::cout << "Opção inválida. Tente novamente.\n"; // Mensagem para opção
                                                         // inválida
      EscolheOpcao(o); // R função para escolher a opção
      break;
    }
  }

  //  opções de Clientes
  void Clientes(int &o) {
    std::cout << "Escolha uma opção para Clientes:\n(1) Cadastrar "
                 "Clientes\n(2) Lista Clientess\n(0) Reiniciar\n";
    std::cin >> o;
    switch (o) {
    case 1:
      CadastrarClientes(); // função para cadastrar cliente
      break;
    case 2:
      ListaClientess(); // função para listar clientes
      break;
    case 0:
      EscolheOpcao(o); // Volta ao menu principal
      break;
    default:
      std::cout << "Opção inválida. Tente novamente.\n"; //  opção inválida
      Clientes(o); // Rechama a função para opções de cliente
      break;
    }
  }

  // Função para cadastrar cliente
  void CadastrarClientes() {
    std::string nome, telefone, email;
    std::cout << "Nome do Clientes: ";
    std::cin.ignore();
    std::getline(std::cin, nome);
    std::cout << "Telefone do Clientes: ";
    std::getline(std::cin, telefone);
    std::cout << "Email do Clientes: ";
    std::getline(std::cin, email);

    std::ofstream arquivo(
        "clientes.txt",
        std::ios::app); // Abrir o arquivo de clientes para acrescentar
    arquivo << nome << "," << telefone << "," << email
            << "\n"; // Escrever os dados do cliente no arquivo
    arquivo.close();

    std::cout << "Clientes cadastrado com sucesso!\n";
    int opcao;
    Clientes(opcao); // menu de cliente
  }

  //  listar clientes
  void ListaClientess() {
    std::ifstream arquivo("clientes.txt"); // arquivo de clientes para leitura
    std::string linha;
    std::cout << "Lista de Clientess:\n";
    while (std::getline(arquivo, linha)) {
      std::istringstream stream(linha);
      std::string nome, telefone, email;
      std::getline(stream, nome, ',');
      std::getline(stream, telefone, ',');
      std::getline(stream, email, ',');

      std::cout << "Nome: " << nome << ", Telefone: " << telefone
                << ", Email: " << email << "\n";
    }
    arquivo.close();

    int opcao;
    Clientes(opcao); // o menu de cliente
  }

  //  opções de Funcionário
  void Funcionarios(int &o) {
    std::cout << "Escolha uma opção para Funcionário:\n(1) Cadastrar "
                 "Funcionário\n(2) Lista Funcionários\n(0) Reiniciar\n";
    std::cin >> o;
    switch (o) {
    case 1:
      CadastrarFuncionarios(); //  função para cadastrar funcionário
      break;
    case 2:
      ListaFuncionarioss(); //  função para listar funcionários
      break;
    case 0:
      EscolheOpcao(o); // o menu principal
      break;
    default:
      std::cout << "Opção inválida. Tente novamente.\n"; // Mensagem para opção
                                                         // inválida
      Funcionarios(o); //  função para opções de funcionário
      break;
    }
  }

  // Função para cadastrar funcionário
  void CadastrarFuncionarios() {
    std::string nome, cargo, telefone;
    std::cout << "Nome do Funcionário: ";
    std::cin.ignore();
    std::getline(std::cin, nome);
    std::cout << "Cargo do Funcionário: ";
    std::getline(std::cin, cargo);
    std::cout << "Telefone do Funcionário: ";
    std::getline(std::cin, telefone);

    std::ofstream arquivo(
        "funcionarios.txt",
        std::ios::app); // arquivo de funcionários para acrescentar
    arquivo << nome << "," << cargo << "," << telefone
            << "\n"; // Escrever os dados do funcionário no arquivo
    arquivo.close();

    std::cout << "Funcionário cadastrado com sucesso!\n";
    int opcao;
    Funcionarios(opcao); // Volta ao menu de funcionário
  }

  //  listar funcionários
  void ListaFuncionarioss() {
    std::ifstream arquivo(
        "funcionarios.txt"); // Abrir o arquivo de funcionários para leitura
    std::string linha;
    std::cout << "Lista de Funcionários:\n";
    while (std::getline(arquivo, linha)) {
      std::istringstream stream(linha);
      std::string nome, cargo, telefone;
      std::getline(stream, nome, ',');
      std::getline(stream, cargo, ',');
      std::getline(stream, telefone, ',');

      std::cout << "Nome: " << nome << ", Cargo: " << cargo
                << ", Telefone: " << telefone << "\n";
    }
    arquivo.close();

    int opcao;
    Funcionarios(opcao); // Voltar no menu de funcionário
  }

  //  opções de Estadia
  void Estadia(int &o) {
    std::cout << "Escolha uma opção para Estadia:\n(1) Registrar Estadia\n(2) "
                 "Lista Estadias\n(0) Reiniciar\n";
    std::cin >> o;
    switch (o) {
    case 1:
      RegistrarEstadia(); //  função para registrar estadia
      break;
    case 2:
      ListaEstadias(); //  função para listar estadias
      break;
    case 0:
      EscolheOpcao(o); // Volta ao menu principal
      break;
    default:
      std::cout << "Opção inválida. Tente novamente.\n"; //  opção inválida
      Estadia(o); // Rechama a função para opções de estadia
      break;
    }
  }

  // Função para registrar estadia
  void RegistrarEstadia() {
    std::string cliente, quarto;
    std::time_t t = std::time(0);
    std::tm *now = std::localtime(&t);

    std::cout << "Nome do Clientes: ";
    std::cin.ignore();
    std::getline(std::cin, cliente);
    std::cout << "Número do QuartosdoHotel: ";
    std::getline(std::cin, quarto);

    std::ofstream arquivo(
        "estadias.txt",
        std::ios::app); // Abrir o arquivo de estadias para acrescentar
    arquivo << cliente << "," << quarto << "," << (now->tm_year + 1900) << '-'
            << (now->tm_mon + 1) << '-' << now->tm_mday// data mes e ano
            << "\n"; // É dados da estadia no arquivo
    arquivo.close();

    std::cout << "Estadia registrada com sucesso!\n";
    int opcao;
    Estadia(opcao); // Volta ao menu de estadia
  }

  // Função para listar estadias
  void ListaEstadias() {
    std::ifstream arquivo(
        "estadias.txt"); // Abre o arquivo de estadias para leitura
    std::string linha;
    std::cout << "Lista de Estadias:\n";
    while (std::getline(arquivo, linha)) {
      std::istringstream stream(linha);
      std::string cliente, quarto, data;
      std::getline(stream, cliente, ',');
      std::getline(stream, quarto, ',');
      std::getline(stream, data, ',');

      std::cout << "Clientes: " << cliente << ", QuartosdoHotel: " << quarto
                << ", Data: " << data << "\n";
    }
    arquivo.close();

    int opcao;
    Estadia(opcao); // Volta ao menu de estadia
  }

  //  opções de QuartosdoHotel
  void QuartosdoHotel(int &o) {
    std::cout << "Escolha uma opção para QuartosdoHotel:\n(1) Cadastrar "
                 "QuartosdoHotel\n(2) Lista QuartosdoHotels\n(0) Reiniciar\n";
    std::cin >> o;
    switch (o) {
    case 1:
      CadastrarQuartosdoHotel(); //  função para cadastrar quarto
      break;
    case 2:
      ListaQuartosdoHotels(); //  função para listar quartos
      break;
    case 0:
      EscolheOpcao(o); // Volta ao menu principal
      break;
    default:
      std::cout << "Opção inválida. Tente novamente.\n"; // Mensagem para opção
                                                         // inválida
      QuartosdoHotel(o); // Rechama a função para opções de quarto
      break;
    }
  }

  //  cadastrar quarto
  void CadastrarQuartosdoHotel() {
    std::string numero, tipo;
    double preco;
    std::cout << "Número do QuartosdoHotel: ";
    std::cin.ignore();
    std::getline(std::cin, numero);
    std::cout << "Tipo do QuartosdoHotel: ";
    std::getline(std::cin, tipo);
    std::cout << "Preço do QuartosdoHotel: ";
    std::cin >> preco;

    std::ofstream arquivo(
        "quartos.txt",
        std::ios::app); // Abre o arquivo de quartos para acrescentar
    arquivo << numero << "," << tipo << "," << preco
            << "\n"; // Escreve os dados do quarto no arquivo
    arquivo.close();

    std::cout << "QuartosdoHotel cadastrado com sucesso!\n";
    int opcao;
    QuartosdoHotel(opcao); // Volta ao menu de quarto
  }

  // listar quartos
  void ListaQuartosdoHotels() {
    std::ifstream arquivo(
        "quartos.txt"); // Abrir o arquivo de quartos para leitura
    std::string linha;
    std::cout << "Lista de QuartosdoHotels:\n";
    while (std::getline(arquivo, linha)) {
      std::istringstream stream(linha);
      std::string numero, tipo;
      double preco;
      std::getline(stream, numero, ',');
      std::getline(stream, tipo, ',');
      stream >> preco;

      std::cout << "Número: " << numero << ", Tipo: " << tipo
                << ", Preço: " << preco << "\n";
    }
    arquivo.close();

    int opcao;
    QuartosdoHotel(opcao); // Volta ao menu de quarto
  }

  //  BaixarEstadias
  void BaixarEstadias(int &o) {
    std::cout << "Escolha uma opção para BaixarEstadias:\n(1) Realizar "
                 "BaixarEstadias\n(2) Lista BaixarEstadiass\n(0) Reiniciar\n";
    std::cin >> o;
    switch (o) {
    case 1:
      RealizarBaixarEstadias(); // Chama a função pa
      break;
    case 2:
      ListaBaixarEstadiass(); // Chama a função
      break;
    case 0:
      EscolheOpcao(o); // Volta ao menu principal
      break;
    default:
      std::cout << "Opção inválida. Tente novamente.\n"; // Mensagem para opção
                                                         // inválida
      BaixarEstadias(o); // Rechama a função para opções de checkout
      break;
    }
  }

  // Função para realizar checkout
  void RealizarBaixarEstadias() {
    std::string cliente, quarto;
    std::cout << "Nome do Clientes: ";
    std::cin.ignore();
    std::getline(std::cin, cliente);
    std::cout << "Número do QuartosdoHotel: ";
    std::getline(std::cin, quarto);

    std::ofstream arquivo(
        "checkouts.txt",
        std::ios::app); // Abre o arquivo de checkouts para acrescentar
    arquivo << cliente << "," << quarto
            << "\n"; // Escrever os dados do checkout no arquivo
    arquivo.close();

    std::cout << "BaixarEstadias realizado com sucesso!\n";
    int opcao;
    BaixarEstadias(opcao); // Volta ao menu de checkout
  }

  // Função para listar checkouts
  void ListaBaixarEstadiass() {
    std::ifstream arquivo(
        "checkouts.txt"); // Abre o arquivo de checkouts para leitura
    std::string linha;
    std::cout << "Lista de BaixarEstadiass:\n";
    while (std::getline(arquivo, linha)) {
      std::istringstream stream(linha);
      std::string cliente, quarto;
      std::getline(stream, cliente, ',');
      std::getline(stream, quarto, ',');

      std::cout << "Clientes: " << cliente << ", QuartosdoHotel: " << quarto
                << "\n";
    }
    arquivo.close();

    int opcao;
    BaixarEstadias(opcao); // Volta ao menu de checkout
  }
};

int main() {
  Hotel hotel;
  int opcao;
  hotel.EscolheOpcao(
      opcao); // Chama a função devolta para escolher a opção do menu principal
  return 0;
}

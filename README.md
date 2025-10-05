#  <p align="center"> Sistema de Gerenciamento de Pizzaria </p>

<p align="center">
  <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
</p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Sobre o Projeto

Este é um sistema completo de gerenciamento para pizzarias desenvolvido com Laravel, aplicando os **princípios SOLID** e boas práticas de programação. O projeto foi desenvolvido com foco em arquitetura limpa, separação de responsabilidades e código de alta qualidade.

O sistema oferece funcionalidades essenciais para o gerenciamento de uma pizzaria moderna, incluindo:

- [Sistema de autenticação JWT seguro](https://jwt.io)
- [Gerenciamento completo de usuários (clientes e funcionários)](https://laravel.com/docs/authentication)
- [CRUD de pizzas com controle de ingredientes e preços](https://laravel.com/docs/eloquent)
- [Sistema de pedidos com cálculo automático de valores](https://laravel.com/docs/eloquent-relationships)
- [Controle de permissões baseado em tipos de usuário](https://laravel.com/docs/authorization)
- [Arquitetura em camadas seguindo SOLID](https://en.wikipedia.org/wiki/SOLID)

O projeto foi desenvolvido pensando em escalabilidade, manutenibilidade e facilidade de extensão para futuras funcionalidades.

## Tecnologias Utilizadas

Este sistema foi construído utilizando as melhores tecnologias e práticas do ecossistema PHP:

- **Laravel 11.x** - Framework PHP moderno e elegante
- **JWT Auth** - Autenticação segura via tokens
- **MySQL** - Banco de dados relacional
- **Eloquent ORM** - Mapeamento objeto-relacional intuitivo
- **Repository Pattern** - Abstração da camada de dados
- **Service Layer** - Centralização das regras de negócio

Se você deseja aprender mais sobre as tecnologias utilizadas, confira a [documentação oficial do Laravel](https://laravel.com/docs) que contém tutoriais completos e exemplos práticos.

Para quem prefere vídeo-aulas, o [Laracasts](https://laracasts.com) oferece milhares de tutoriais sobre Laravel, PHP moderno, testes automatizados e muito mais.

## Arquitetura do Sistema

O projeto segue uma arquitetura em camadas bem definida:

```
Rotas → Controllers → Services → Repositories → Models → Database
```

- **Rotas**: Apenas definem os endpoints da API
- **Controllers**: Recebem requisições e chamam os services apropriados
- **Services**: Contêm toda a lógica de negócio e regras da aplicação
- **Repositories**: Responsáveis pela comunicação com o banco de dados
- **Models**: Representam as entidades do sistema

## Princípios SOLID Aplicados

✅ **Single Responsibility** - Cada classe tem uma única responsabilidade  
✅ **Open/Closed** - Aberto para extensão, fechado para modificação  
✅ **Liskov Substitution** - Substituição de interfaces sem quebrar funcionalidades  
✅ **Interface Segregation** - Interfaces específicas e bem definidas  
✅ **Dependency Inversion** - Dependência de abstrações, não de implementações

## Instalação e Configuração

```bash
# Instalar dependências
composer install

# Instalar JWT Auth
composer require tymon/jwt-auth

# Gerar chave JWT
php artisan jwt:secret

# Configurar banco de dados no .env
# DB_DATABASE=pizzaria

# Executar migrations
php artisan migrate

# Popular banco com dados de teste
php artisan db:seed

# Iniciar servidor
php artisan serve
```

## Funcionalidades Principais

###  Autenticação
- Registro de novos usuários
- Login com JWT
- Logout seguro
- Verificação de perfil

###  Gerenciamento de Usuários
- CRUD completo de usuários
- Diferenciação entre clientes e funcionários
- Validação de dados e segurança

###  Gerenciamento de Pizzas
- Cadastro exclusivo para funcionários
- Controle de ingredientes e preços
- Diferentes tamanhos disponíveis
- Sistema de ativação/desativação

###  Sistema de Pedidos
- Criação de pedidos por clientes
- Adição de ingredientes extras (R$ 3,00 cada)
- Cálculo automático do valor total
- Controle de status do pedido
- Histórico completo

## Regras de Negócio

- ✅ Pedidos devem conter no mínimo 1 pizza
- ✅ Apenas funcionários podem gerenciar pizzas
- ✅ Clientes visualizam apenas seus próprios pedidos
- ✅ Valores são calculados automaticamente
- ✅ Ingredientes extras alteram o preço final
- ✅ Pedidos finalizados não podem ser alterados

## Endpoints da API

Documentação completa disponível nos arquivos:
- `GUIA_COMPLETO.md` - Instalação e uso detalhado
- `EXEMPLOS_PRATICOS.md` - Casos de uso reais
- `COMANDOS_RAPIDOS.sh` - Setup rápido


## Contribuindo

Contribuições são sempre bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Código de Conduta

Para garantir que a comunidade seja acolhedora para todos, por favor revise e siga o [Código de Conduta](https://laravel.com/docs/contributions#code-of-conduct).

## Vulnerabilidades de Segurança

Se você descobrir alguma vulnerabilidade de segurança neste projeto, por favor envie um e-mail para o mantenedor. Todas as vulnerabilidades serão tratadas prontamente.

## Licença

Este projeto é um software de código aberto licenciado sob a [licença MIT](https://opensource.org/licenses/MIT).

---

**Desenvolvido usando Laravel e princípios SOLID**

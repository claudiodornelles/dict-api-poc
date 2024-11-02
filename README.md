# Prova de Conceito - Aplicação Java com Arquitetura de Monólito Modular

Este projeto é uma prova de conceito para demonstrar a implementação de uma aplicação Java utilizando Spring Boot e Gradle, com uma arquitetura de Monólito Modular. A aplicação é baseada na API do Diretório de Identificadores de Contas Transacionais (DICT) do Banco Central do Brasil (BACEN), simulando uma integração com a API para validação de chaves Pix.

## Objetivo

O objetivo é explorar a arquitetura de Monólito Modular, separando as responsabilidades da aplicação em módulos independentes que compartilham uma base de código e são implantados juntos. Essa arquitetura permite um desenvolvimento modularizado dentro de uma única aplicação, facilitando a manutenção e a escalabilidade ao longo do tempo.

## Estrutura do Projeto

A estrutura do projeto é organizada em módulos, conforme os principais casos de uso da API DICT:

```
dict-api-poc/
├── src: Contém as definições e configurações centrais da aplicação.
├── modulos/
│   ├── antifraude: Responsável pelo gerenciamento de fraudes no DICT.
│   ├── diretiorio: Implementa as funcionalidades de consulta, criação, atualização e remoção de chaves PIX.
│   └── reivindicacao: Implementa as funcionalidades de criação, consulta, listagem, recebimento, confirmação, cancelamento e conclusão de reivindicações de posse de chaves PIX.
```
Cada módulo é implementado em pacotes separados e possui seu próprio conjunto de serviços, repositórios e controladores, permitindo uma separação clara das responsabilidades.
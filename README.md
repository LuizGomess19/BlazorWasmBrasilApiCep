# BlazorWasmBrasilApiCep

Aplicação desenvolvida em **Blazor WebAssembly (.NET 8)** para consulta de endereços via CEP utilizando a API pública da **BrasilAPI**.

Projeto prático desenvolvido para a disciplina **Dev Web, Mobile e Jogos** (Professor Daniel Henrique Matos de Paiva).

---

## 🚀 Funcionalidades

- Consulta de endereços a partir do CEP (8 dígitos numéricos).
- Consumo da API da BrasilAPI (`GET https://brasilapi.com.br/api/cep/v1/{cep}`).
- Deserialização da resposta JSON em modelos fortemente tipados (`Cep` e `Ibge`).
- Exibição reativa das informações na interface do Blazor WebAssembly:
  - CEP
  - Logradouro (Rua/Avenida)
  - Bairro
  - Cidade e Estado (UF)
  - Serviço provedor da busca
  - Dados de código do IBGE (Cidade e Estado)
- Validação de entrada e tratamento de erros (CEP não encontrado, erros de rede, etc.).

---

## 🛠️ Tecnologias Utilizadas

- **C# / .NET 8**
- **Blazor WebAssembly** (Standalone)
- **Bootstrap 5** (Layout e estilização)
- **BrasilAPI** (Provedor dos dados de CEP e IBGE)

---

## 📂 Estrutura do Projeto

```text
BlazorWasmBrasilApiCep/
├── Layout/
│   ├── MainLayout.razor
│   ├── MainLayout.razor.css
│   ├── NavMenu.razor
│   └── NavMenu.razor.css
├── Models/
│   ├── Cep.cs
│   └── Ibge.cs
├── Pages/
│   ├── Counter.razor
│   ├── Home.razor
│   └── Weather.razor
├── Properties/
│   └── launchSettings.json
├── wwwroot/
│   ├── css/
│   ├── favicon.png
│   ├── icon-192.png
│   ├── index.html
│   └── sample-data/
├── _Imports.razor
├── App.razor
├── BlazorWasmBrasilApiCep.csproj
├── Program.cs
└── README.md
```

---

## ▶️ Como Executar

### Pré-requisitos
- [.NET SDK 8.0+](https://dotnet.microsoft.com/download)

### Passos
1. Clone o repositório:
   ```bash
   git clone https://github.com/LuizGomess19/BlazorWasmBrasilApiCep.git
   cd BlazorWasmBrasilApiCep
   ```

2. Restaure as dependências e execute a aplicação:
   ```bash
   dotnet run
   ```

3. Abra a URL informada no terminal (normalmente `http://localhost:5062` ou porta dinâmica) no navegador e digite um CEP para consultar (exemplo: `30130000`).

# Decodificador de VIN Volkswagen

Um decodificador completo e responsivo para números de identificação de veículos (VIN) da Volkswagen, baseado na documentação oficial e especificações ISO 3779.

🌐 **Demo Online**: [https://phnahes.github.io/vw-vin-decoder/](https://phnahes.github.io/vw-vin-decoder/)

## 🚗 Sobre o Projeto

Este projeto implementa um decodificador de VIN específico para veículos Volkswagen, capaz de identificar modelos, anos, plantas de fabricação e validar a integridade do código.

### ✨ Funcionalidades Principais

- **Validação completa de VIN** (17 caracteres conforme ISO 3779)
- **Cálculo de dígito verificador** para validação de integridade
- **Identificação de modelos** baseada em padrões reais de VINs
- **Mapeamento de anos** (2000-2027) com especificação oficial
- **Identificação de plantas** de fabricação VW em todo o mundo
- **Interface responsiva** com design moderno e limpo
- **Decodificação automática** ao digitar 17 caracteres
- **Exemplos pré-carregados** para testes rápidos

## 🌍 Códigos WMI Suportados

O sistema reconhece os seguintes códigos World Manufacturer Identifier (WMI):

### Volkswagen Europa
- **WVW** - Volkswagen Cars (Europa)
- **WVG** - Volkswagen SUVs (Europa) 
- **WV1** - Volkswagen Commercials (Europa)
- **WV2** - Volkswagen Bus/Van (Europa)
- **WV3** - Volkswagen Trucks (Europa)

### Volkswagen Américas
- **9BW** - Volkswagen Brasil
- **3VW** - Volkswagen México
- **8AW** - Volkswagen Argentina
- **1VW** - Volkswagen USA

### Audi
- **WAU** - Audi (Alemanha)
- **TRU** - Audi Hungria
- **93V** - Audi Brasil

## 🏭 Plantas de Fabricação Identificadas

O sistema identifica mais de 30 plantas de fabricação Volkswagen em todo o mundo:

### Brasil
- **F** - Ipiranga/Resende, Brasil
- **P** - Anchieta, Brasil
- **T** - Taubaté, Brasil
- **4** - Curitiba, Brasil

### México
- **M** - Puebla, México

### Argentina
- **8** - General Pacheco, Argentina

### Alemanha
- **W** - Wolfsburg, Alemanha
- **E** - Emden, Alemanha
- **A** - Ingolstadt, Alemanha
- **H** - Hanover, Alemanha
- **K** - Osnabrück, Alemanha
- **N** - Neckarsulm, Alemanha
- **S** - Salzgitter, Alemanha
- **8** - Dresden, Alemanha

### Outros Países
- **B** - Bruxelas, Bélgica
- **C** - Chattanooga, EUA
- **D** - Bratislava, Eslováquia
- **G** - Graz, Áustria
- **L** - Lagos, Nigéria
- **R** - Martorell, Espanha
- **U** - Uitenhage, África do Sul
- **V** - Palmela, Portugal
- **X** - Poznan, Polônia
- **Y** - Pamplona, Espanha
- **1** - Győr, Hungria
- **2** - Anting, China
- **3** - Changchun, China

## 🎯 Detecção Inteligente de Modelos

### Volkswagen Brasil (9BW)
O sistema identifica modelos brasileiros baseado nos códigos VDS (posições 4-5):

- **CH** - Nivus
- **AH** - Polo
- **AJ** - Polo/Golf
- **BJ** - T-Cross
- **KB** - Saveiro
- **DH/DJ** - Virtus

### Volkswagen México (3VW)
- **AE** - Jetta

### Volkswagen Argentina (8AW)
- **BJ** - Taos

### Base de Dados Completa
O sistema inclui uma base de dados com mais de 400 códigos de modelo VW de todas as regiões, incluindo:
- Modelos históricos (Beetle, Golf, Passat)
- Modelos atuais (T-Cross, Nivus, Virtus)
- Veículos comerciais (Caddy, Transporter, Crafter)
- Veículos elétricos (ID.3, ID.4, ID.Buzz)

## 📋 Estrutura do VIN

O sistema segue a estrutura oficial do VIN conforme ISO 3779:

### Posições 1-3: World Manufacturer Identifier (WMI)
- **Posição 1**: Região de fabricação
  - A-H: África
  - J-R: Ásia
  - S-Z: Europa
  - 1-5: América do Norte
  - 6-7: Oceania
  - 8-0: América do Sul
- **Posição 2**: Fabricante (geralmente 'V' para VW)
- **Posição 3**: Tipo de veículo

### Posições 4-9: Vehicle Descriptor Section (VDS)
- **Posições 4-6**: Códigos específicos do modelo
- **Posições 7-8**: Descritor do veículo VW
- **Posição 9**: Dígito verificador (posição 8)

### Posições 10-17: Vehicle Identifier Section (VIS)
- **Posição 10**: Ano do modelo
- **Posição 11**: Planta de fabricação
- **Posições 12-17**: Número serial único

## 📅 Mapeamento de Anos

O sistema utiliza o mapeamento oficial de anos:

| Código | Ano | Código | Ano | Código | Ano |
|--------|-----|--------|-----|--------|-----|
| Y | 2000 | A | 2010 | L | 2020 |
| 1 | 2001 | B | 2011 | M | 2021 |
| 2 | 2002 | C | 2012 | N | 2022 |
| 3 | 2003 | D | 2013 | P | 2023 |
| 4 | 2004 | E | 2014 | R | 2024 |
| 5 | 2005 | F | 2015 | S | 2025 |
| 6 | 2006 | G | 2016 | T | 2026 |
| 7 | 2007 | H | 2017 | V | 2027 |
| 8 | 2008 | J | 2018 | W | 2028 |
| 9 | 2009 | K | 2019 | X | 2029 |

## 🎨 Interface e Design

### Características da Interface
- **Design limpo**: Esquema de cores claras e modernas
- **Responsivo**: Adapta-se perfeitamente a dispositivos móveis
- **Mobile-first**: Otimizado para smartphones e tablets
- **Tipografia moderna**: Usando fontes do sistema para melhor legibilidade
- **Feedback visual**: Indicadores claros de VIN válido/inválido

### Funcionalidades da Interface
- **Decodificação automática**: Quando você digita 17 caracteres, decodifica automaticamente
- **Exemplos pré-carregados**: VINs de exemplo para testes rápidos
- **Grid de resultados**: Informações organizadas em cards responsivos
- **Status visual**: Indicadores de sucesso/erro com cores apropriadas

## 🚀 Como Usar

### Uso Básico

#### 🌐 Versão Online (Recomendado)
1. Acesse: [https://phnahes.github.io/vw-vin-decoder/](https://phnahes.github.io/vw-vin-decoder/)
2. Digite um VIN de 17 caracteres no campo de entrada
3. O sistema decodificará automaticamente quando você digitar 17 caracteres
4. Clique em "Decodificar" para processar manualmente
5. Use "Limpar" para resetar o campo

#### 💻 Versão Local
1. Clone este repositório: `git clone https://github.com/phnahes/vw-vin-decoder.git`
2. Abra o arquivo `index.html` em qualquer navegador moderno
3. Siga os mesmos passos da versão online


### Interpretando os Resultados

O sistema exibe as seguintes informações:

- **Status**: ✓ VIN Válido ou ✗ VIN Inválido
- **VIN**: Número completo do VIN
- **WMI**: Código do fabricante com região
- **Modelo**: Modelo identificado com código VDS
- **Ano**: Código do ano e ano correspondente
- **Planta**: Código da planta e localização
- **Serial**: Número serial do veículo
- **VDS**: Seção de descrição do veículo
- **VIS**: Seção de identificação do veículo
- **Dígito Verificador**: Dígito calculado vs. dígito do VIN

## 🔧 Implementação Técnica

### Tecnologias Utilizadas
- **HTML5**: Estrutura semântica
- **CSS3**: Estilos modernos com CSS Grid e Flexbox
- **JavaScript ES6+**: Lógica de decodificação
- **Design Responsivo**: Media queries para diferentes dispositivos

### Estrutura do Código
- **Validação de VIN**: Função `calcCheckDigit()` para validação ISO 3779
- **Decodificação**: Função `decodeLocal()` para processamento completo
- **Identificação de modelos**: Função `inferModel()` com lógica inteligente
- **Mapeamentos**: Objetos com códigos WMI, plantas e anos
- **Interface**: Função `renderSingle()` para exibição dos resultados

### Algoritmo de Validação
O sistema utiliza o algoritmo oficial ISO 3779:
1. Converte caracteres para valores numéricos
2. Aplica pesos específicos para cada posição
3. Calcula soma ponderada
4. Determina dígito verificador (resto da divisão por 11)
5. Compara com dígito verificador do VIN


### Especificações Técnicas
- **Estrutura VIN**: Conforme ISO 3779
- **Códigos WMI**: Baseados em registros oficiais
- **Mapeamento de anos**: Especificação oficial VW
- **Códigos de plantas**: Documentação oficial das fábricas

### Exemplos de Padrões
- Padrões de VINs brasileiros identificados
- Padrões de VINs de diferentes regiões (México, Argentina, Brasil)
- Modelos atuais e históricos da Volkswagen
- **Dados reais confirmados**: Polo 1.0 (9BWAH5BZ7RT600182) com informações completas de motor, transmissão e especificações

## 🛠️ Desenvolvimento

### Estrutura do Projeto
```
vw-vin-decoder/
├── index.html          # Arquivo principal com toda a aplicação
└── README.md           # Este arquivo de documentação
```

### Funcionalidades Implementadas
- ✅ Validação completa de VIN
- ✅ Decodificação de WMI, VDS e VIS
- ✅ Identificação de modelos VW
- ✅ Mapeamento de anos e plantas
- ✅ Interface responsiva
- ✅ Exemplos pré-carregados
- ✅ Decodificação automática


## 📄 Licença

Este projeto é de código aberto e pode ser usado livremente para fins educacionais e comerciais.

---
---
title: Recálculo do Excel
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- cálculo forçado [excel 2007],recálculo seletivo [Excel 2007],funções [Excel 2007], volátil,modos de cálculo,células recalculadas [Excel 2007],dependência [Excel 2007],cálculo especificado de planilha [Excel 2007],recálculo [Excel 2007],reconstrução de árvore de pasta de trabalho [Excel 2007],cálculo de intervalo [Excel 2007],recálculo do Excel,funções voláteis [Excel 2007],funções [Excel 2007], não volátil,cálculo de planilha ativa [Excel 2007],células sujas [Excel 2007],funções não voláteis [Excel 2007],recálculo forçado [Excel 2007]
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 07deec5ad104c59074567725d6abf9b66711e351
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703346"
---
# <a name="excel-recalculation"></a>Recálculo do Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O usuário pode acionar o recálculo no Microsoft Excel de várias maneiras, por exemplo:
  
- Inserindo novos dados (se o Excel estiver no Modo de recálculo automático, descrito mais adiante neste tópico).
    
- Explicitamente instruindo o Excel a recalcular uma pasta de trabalho no todo ou em parte.
    
- Excluindo ou inserindo uma linha ou coluna.
    
- Salvando uma pasta de trabalho enquanto a opção **Recalcular antes de salvar** está definida. 
    
- Executando determinadas ações de Filtro Automático.
    
- Clicando duas vezes em um divisor de linha ou coluna (no modo de Cálculo automático).
    
- Adicionando, editando ou excluindo um nome definido.
    
- Renomeando uma planilha.
    
- Alterando a posição de uma planilha em relação a outras planilhas.
    
- Ocultando ou como reexibindo linhas, mas não colunas.
    
> [!NOTE]
> Este tópico não faz distinção entre o usuário que pressiona diretamente uma tecla ou clica no mouse e as tarefas que estão sendo executadas por um comando ou macro. O usuário executa o comando ou faz algo para que o comando seja executado para que isso ainda seja considerado uma ação do usuário. Portanto, a frase "o usuário" também significa "o usuário ou um comando ou processo iniciado pelo usuário". 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>Dependência, Células Sujas e Células Recalculadas

O cálculo de planilhas no Excel pode ser visto como um processo em três etapas:
  
1. Construção de uma árvore de dependência
    
2. Construção de uma cadeia de cálculo
    
3. Recálculo de células
    
A árvore de dependência informa ao Excel quais células dependem de quais outras ou, de forma equivalente, quais células são precedentes a quais outras. Com base nessa árvore, o Excel cria uma cadeia de cálculo. A cadeia de cálculo lista todas as células que contêm fórmulas na ordem em que devem ser calculadas. Durante o recálculo, o Excel revisa essa cadeia se encontra uma fórmula que depende de uma célula que ainda não foi calculada. Nesse caso, a célula que está sendo calculada e seus dependentes são movidos para baixo na cadeia. Por esse motivo, os tempos de cálculo geralmente podem melhorar em uma planilha que acaba de ser aberta nos primeiros ciclos de cálculo.
  
Quando uma alteração estrutural é feita em uma pasta de trabalho, por exemplo, quando uma nova fórmula é inserida, o Excel recria a árvore de dependência e a cadeia de cálculo. Quando novos dados ou novas fórmulas são inseridos, o Excel marca todas as células que dependem de novos dados como precisando de recálculo. As células marcadas dessa maneira são conhecidas como *sujas*. Todos os dependentes diretos e indiretos são marcados como sujos. Portanto, se B1 depender de A1, e C1 depender de B1, quando A1 for alterado, tanto B1 quanto C1 serão marcados como sujos. 
  
Se uma célula depender de si mesma, direta ou indiretamente, o Excel detectará a referência circular e avisará o usuário. Isso geralmente é uma condição de erro que o usuário deve corrigir, e o Excel fornece ferramentas gráficas e de navegação muito úteis para ajudar o usuário a encontrar a origem da dependência circular. Em alguns casos, você pode querer deliberadamente que essa condição exista. Por exemplo, você pode querer executar um cálculo iterativo em que o ponto inicial da próxima iteração é o resultado da iteração anterior. O Excel dá suporte ao controle de cálculos iterativos por meio da caixa de diálogo de opções de cálculo.
  
Depois de marcar as células como sujas, quando um recálculo é feito em seguida, o Excel reavalia o conteúdo de cada célula suja na ordem ditada pela cadeia de cálculo. No exemplo fornecido anteriormente, isso significa que B1 vem primeiro e, em seguida, C1. Esse recálculo ocorrerá imediatamente após o Excel terminar de marcar as células como sujas se o modo de recálculo for automático. Caso contrário, ocorrerá mais tarde.
  
A partir do Microsoft Excel 2002, o objeto **Range** no VBA (Visual Basic for Applications) dá suporte a um método, **Range.Dirty**, que marca células como precisando de cálculo. Quando usado em conjunto com o método **Range.Calculate** (veja a próxima seção), ele permite o recálculo forçado de células em determinado intervalo. Isso é útil quando você está executando um cálculo limitado durante uma macro, em que o modo de cálculo é definido como manual, para evitar a sobrecarga de cálculo de células não relacionadas à função de macro. Os métodos de cálculo de intervalo não estão disponíveis por meio da API de C. 
  
No Excel 2002 e versões anteriores, o Excel criava uma cadeia de cálculo para cada planilha em cada pasta de trabalho aberta. Isso gerava alguma complexidade na forma como os vínculos entre as planilhas eram tratados e exigia algum cuidado para garantir que o recálculo fosse eficiente. Em particular, no Excel 2000, você deve minimizar as dependências de planilha cruzada e nomear as planilhas em ordem alfabética, para que as planilhas que dependem de outras planilhas venham em ordem alfabética após as planilhas das quais dependem.
  
No Excel 2007, a lógica foi aprimorada para habilitar o recálculo em vários threads, de forma que as seções da cadeia de cálculo não sejam interdependentes e possam ser calculadas ao mesmo tempo. Você pode configurar o Excel para usar vários threads em um computador com processador único ou um único thread em um computador com vários processadores ou vários núcleos. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>UDFs (Funções Assíncronas Definidas pelo Usuário)

Quando um cálculo encontra uma UDF assíncrona, ele salva o estado da fórmula atual, inicia a UDF e continua avaliando o restante das células. Quando o cálculo termina de avaliar as células, o Excel aguarda a conclusão das funções assíncronas, se ainda há funções assíncronas em execução. À medida que cada função assíncrona relata resultados, o Excel conclui a fórmula e, em seguida, executa uma nova passagem de cálculo para recalcular células que usam a célula com a referência à função assíncrona.
  
## <a name="volatile-and-non-volatile-functions"></a>Funções voláteis e não voláteis

O Excel dá suporte ao conceito de uma função volátil, ou seja, uma cujo valor não pode ser presumido como sendo o mesmo de um momento para o outro, mesmo que nenhum de seus argumentos tenha sido alterado. O Excel reavalia células que contêm funções voláteis, juntamente com todos os dependentes, sempre que realiza o recálculo. Por essa razão, a dependência excessiva de funções voláteis pode aumentar o tempo de recálculo. Use-as com moderação.
  
As seguintes funções do Excel são voláteis:
  
- **AGORA**
    
- **HOJE**
    
- **ALEATÓRIOENTRE**
    
- **DESLOCAMENTO**
    
- **INDIRETO**
    
- **INFORMAÇÕES** (dependendo de seus argumentos) 
    
- **CÉLULA** (dependendo de seus argumentos) 
    
- **SOMASE** (dependendo de seus argumentos) 
    
Tanto o VBA quanto a API de C dão suporte a maneiras de informar ao Excel que uma UDF (função definida pelo usuário) deve ser tratada como volátil. Usando o VBA, a UDF é declarada como volátil da maneira a seguir.
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

Por padrão, o Excel presume que as UDFs do VBA não são voláteis. O Excel só descobre que uma UDF é volátil quando a chama pela primeira vez. Uma UDF volátil pode ser alterada de volta para não volátil, como neste exemplo.
  
Usando a API de C, você pode registrar uma função XLL como volátil antes de sua primeira chamada. Isso também permite que você ative e desative o status volátil de uma função de planilha.
  
Por padrão, o Excel lida com UDFs XLL que aceitam argumentos de intervalo e que são declaradas como equivalentes de planilha de macro como voláteis. Você pode desativar esse estado padrão usando a função **xlfVolatile** quando a UDF é chamada pela primeira vez. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Modos de Cálculo, Comandos, Recálculo Seletivo e Tabelas de Dados

O Excel tem três modos de cálculo:
  
- Automático
    
- Automático, Exceto Tabelas
    
- Manual
    
Quando o cálculo é definido como automático, o recálculo ocorre após cada entrada de dados e após certos eventos, como os exemplos fornecidos na seção anterior. Para pastas de trabalho muito grandes, o tempo de recálculo pode ser tão longo que os usuários devem limitar quando isso ocorre, ou seja, recalcular somente quando necessário. Para habilitar isso, o Excel dá suporte ao modo manual. O usuário pode selecionar o modo por meio do sistema de menu do Excel ou programaticamente usando VBA, COM ou a API de C.
  
Tabelas de dados são estruturas especiais em uma planilha. Primeiro, o usuário configura o cálculo de um resultado em uma planilha. Isso depende de uma ou duas entradas variáveis e outros parâmetros. O usuário pode então criar uma tabela de resultados para um conjunto de valores para uma das entradas principais ou ambas. A tabela é criada usando o **Assistente de Tabela de Dados**. Depois que a tabela é configurada, o Excel conecta as entradas uma a uma no cálculo e copia o valor resultante na tabela. Como uma ou duas entradas podem ser usadas, as tabelas de dados podem ser unidimensionais ou bidimensionais. 
  
O recálculo de tabelas de dados é tratado de forma ligeiramente diferente:
  
- O recálculo é tratado de forma assíncrona para o recálculo regular da pasta de trabalho, assim, as tabelas grandes demoram mais para serem recalculadas do que o restante da pasta de trabalho.
    
- Referências circulares são toleradas. Se o cálculo usado para obter o resultado depender de um ou mais valores da tabela de dados, o Excel não retornará um erro para a dependência circular. 

- Tabelas de dados não usam cálculo multi-threaded.
    
Dada a maneira diferente como o Excel lida com o recálculo de tabelas de dados e o fato de que tabelas grandes que dependem de cálculos complexos ou demorados podem levar muito tempo para serem calculadas, o Excel permite desabilitar o cálculo automático de tabelas de dados. Para fazer isso, defina o modo de cálculo como Automático, exceto Tabelas de Dados. Quando o cálculo está neste modo, o usuário recalcula as tabelas de dados pressionando F9 ou usando alguma operação programática equivalente.
  
O Excel expõe métodos pelos quais você pode alterar o modo de recálculo e controlar o recálculo. Esses métodos foram aprimorados de versão para versão para permitir controle mais preciso. Os recursos da API de C a esse respeito refletem os que estavam disponíveis na versão 5 do Excel e, assim, não fornecem o mesmo controle de que você dispõe ao usar o VBA em versões mais recentes. 
  
Usados com mais frequência quando o Excel está no modo de cálculo manual, esses métodos permitem o cálculo seletivo de pastas de trabalho, planilhas e intervalos, o recálculo completo de todas as pastas de trabalho abertas e até a reconstrução completa da árvore de dependência e da cadeia de cálculo.
  
### <a name="range-calculation"></a>Cálculo de Intervalo

Pressionamento de teclas: nenhum
  
VBA: **Range.Calculate** (introduzido no Excel 2000; alterado no Excel 2007) e **Range.CalculateRowMajorOrder** (introduzido no Excel 2007) 
  
API de C: sem suporte
  
- **Modo manual**
    
    Recalcula apenas as células no intervalo determinado, independentemente de serem sujas ou não. O comportamento do método **Range.Calculate** foi alterado no Excel 2007; no entanto, o comportamento antigo ainda tem suporte no método **Range.CalculateRowMajorOrder**. 
    
- **Automático Automático, Exceto Modos de Tabelas**
    
    Recalcula a pasta de trabalho, mas não força o recálculo do intervalo nem de nenhuma célula no intervalo.
    
### <a name="active-worksheet-calculation"></a>Cálculo de Planilha Ativa

Pressionamento de teclas: Shift+F9
  
VBA: **ActiveSheet.Calculate**
  
API do C: **xlcCalculateDocument**
  
- **Todos os modos**
    
    Recalcula as células marcadas para cálculo somente na planilha ativa.
    
### <a name="specified-worksheet-calculation"></a>Cálculo de Planilha Especificada

Pressionamento de teclas: nenhum
  
VBA: **Worksheets(** reference **).Calculate**
  
API de C: sem suporte
  
- **Todos os modos**
    
    Recalcula as células sujas e seus dependentes somente na planilha especificada. Reference é o nome da planilha como uma cadeia de caracteres ou o número do índice na pasta de trabalho relevante.
    
    O Excel 2000 e versões posteriores expõem uma propriedade de planilha **Boolean**, a propriedade **EnableCalculation**. Configurar isso como **True** em vez de **False** faz com que todas as células na planilha especificada sejam sujas. Nos modos automáticos, isso também dispara um recálculo de toda a pasta de trabalho. 
    
    No modo manual, o código a seguir causa o recálculo somente da planilha ativa.
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>Reconstrução de Árvore de Pasta de Trabalho e Recálculo Forçado

Pressionamento de teclas: Ctrl+Alt+Shift+F9 (introduzido no Excel 2002)
  
VBA: **Workbooks(** reference **).ForceFullCalculation** (introduzido no Excel 2007) 
  
API de C: sem suporte
  
- **Todos os modos**
    
    Faz com que o Excel reconstrua a árvore de dependência e a cadeia de cálculo de determinada pasta de trabalho e força um recálculo de todas as células que contêm fórmulas.
    
### <a name="all-open-workbooks"></a>Todas as Pastas de Trabalho Abertas

Pressionamento de teclas: F9
  
VBA: **Application.Calculate**
  
API do C: **xlcCalculateNow**
  
- **Todos os modos**
    
    Recalcula todas as células que o Excel marcou como sujas, isto é, dependentes de dados voláteis ou alterados e células programaticamente marcadas como sujas. Se o modo de cálculo é Automático, Exceto Tabelas, calcula as tabelas que exigem atualização e também todas as funções voláteis e seus dependentes.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Reconstrução de Árvore de Todas as Pastas de Trabalho Abertas e Cálculo Forçado

Pressionamento de teclas: Ctrl+Alt+F9
  
VBA: **Application.CalculateFull**
  
API de C: sem suporte
  
- **Todos os modos**
    
    Recalcula todas as células em todas as pastas de trabalho abertas. Se o modo de cálculo é Automático, Exceto Tabelas, força as tabelas a serem recalculadas.
    
## <a name="see-also"></a>Confira também



[Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Tipos de dados usados pelo Excel](data-types-used-by-excel.md)
  
[Gerenciamento de Memória no Excel](memory-management-in-excel.md)
  
[Conceitos de programação do Excel](excel-programming-concepts.md)


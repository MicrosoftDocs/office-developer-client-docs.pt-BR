---
title: Recálculo do Excel
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- cálculo de forçado [excel 2007], recálculo seletivo [Excel 2007], funções voláteis, cálculo de [Excel 2007], modos, células recalculadas [Excel 2007], [Excel 2007], a dependência especificado cálculo de planilha [Excel 2007], recálculo [Excel 2007 ], reconstrução de árvore da pasta de trabalho [Excel 2007], [Excel 2007], [de funções não voláteis de células de recálculo do Excel, funções voláteis [Excel 2007], funções de cálculo de planilha não voláteis, active [Excel 2007], [Excel 2007], dirty de cálculo de intervalo [Excel 2007] Excel 2007], forçado recálculo [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 70ca322173fb76eb1871d841b6246b62b3a5000a
ms.sourcegitcommit: 539bc9a767ede52cb17c1b11ef7fac2fecd96fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/22/2018
ms.locfileid: "22554166"
---
# <a name="excel-recalculation"></a>Recálculo do Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O usuário pode disparar o recálculo no Microsoft Excel de várias maneiras, por exemplo:
  
- Inserir novos dados (se o Excel está no modo de recálculo automático, descrito mais adiante neste tópico).
    
- Instruindo explicitamente Excel recalcule todo ou parte de uma pasta de trabalho.
    
- A exclusão ou inserir uma linha ou coluna.
    
- Salvando uma pasta de trabalho enquanto o **Recalcular antes de salvar** a opção é definida. 
    
- A execução de determinadas ações Autofilter.
    
- Clicando duas vezes em um divisor de coluna ou linha (no modo de cálculo automático).
    
- Adicionando, editando ou excluindo um nome definido.
    
- Renomear uma planilha.
    
- Alterar a posição de uma planilha em relação a outras planilhas.
    
- Ocultar ou Mostrar linhas, mas não de colunas.
    
> [!NOTE]
> Este tópico não faz distinção entre o usuário diretamente pressionando uma tecla ou clicando o mouse e essas tarefas que está sendo feitas por um comando ou uma macro. O usuário executa o comando ou faz algo para fazer com que o comando seja executado para que ela ainda será considerada uma ação do usuário. Portanto, a frase "usuário" significa também ", o usuário ou um comando ou processo iniciado pelo usuário." 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>A dependência, células Dirty e células recalculadas

Cálculo de planilhas do Excel pode ser exibido como um processo de três estágios:
  
1. Construção de uma árvore de dependência
    
2. Construção de uma cadeia de cálculo
    
3. Recálculo de células
    
A árvore de dependência informa sobre quais células dependem do que outros recursos do Excel ou maneira equivalente, quais células são precedentes para que outros recursos. Na árvore de, Excel constrói uma cadeia de cálculo. A cadeia de cálculo lista todas as células que contêm fórmulas na ordem na qual deve ser calculados. Durante o recálculo, o Excel revisa essa cadeia se encontrar uma fórmula que depende de uma célula que ainda não foi calculada. Nesse caso, a célula que está sendo calculada e seus dependentes são movidos para baixo a cadeia. Por esse motivo, os tempos de cálculo geralmente podem melhorar em uma planilha que acabou foi aberta em alguns ciclos de cálculo da primeiro.
  
Quando uma alteração estrutural é feita de uma pasta de trabalho, por exemplo, quando uma nova fórmula é inserida, o Excel reconstrói a cadeia de cálculo e a árvore de dependência. Quando novos dados ou novas fórmulas são inseridas, Excel marcará todas as células que dependem de novos dados como precisam de recálculo. As células que são marcadas dessa forma são conhecidas como *sujo* . Todos os dependentes diretos e indiretos são marcados como sujo para que se B1 depende A1 e C1 depende B1, quando A1 é alterada, B1 e C1 estão marcado como sujo. 
  
Se uma célula depende, direta ou indiretamente, em si, o Excel detecta a referência circular e avisa o usuário. Normalmente, isso é uma condição de erro que o usuário deve corrigir e Excel fornece ferramentas muito úteis de gráficas e de navegação para ajudar o usuário para localizar a origem da dependência circular. Em alguns casos, você pode querer deliberadamente essa condição de existir. Por exemplo, talvez você queira executar um cálculo repetitivo onde o ponto de partida para a próxima iteração é o resultado da iteração anterior. Excel suporta controle de cálculos repetitivo através da caixa de diálogo de opções de cálculo.
  
Depois de marcar células como sujo, quando um recálculo é feito em seguida, o Excel revê o conteúdo de cada célula dirty na ordem ditada pela cadeia de cálculo. No exemplo fornecido anteriormente, isso significa que B1 é o primeiro e, em seguida, C1. Este recálculo ocorre imediatamente após o Excel concluir a marcação de células como sujo se o modo de recálculo é automático; Caso contrário, ele ocorre posteriormente.
  
O objeto de **intervalo** no Microsoft Visual Basic for Applications (VBA) a partir do Microsoft Excel 2002, oferece suporte a um método, **Range.Dirty**, que marca células como precisando de cálculo. Quando ele é usado em conjunto com o método **intervalo** . (consulte a próxima seção), ele permite que o recálculo forçado de células em um determinado intervalo. Isso é útil quando você executa um cálculo limitadas durante uma macro, onde o modo de cálculo é definido como manual, para evitar a sobrecarga de cálculo de células não relacionadas para a função de macro. Métodos de cálculo do intervalo não estão disponíveis por meio da API C. 
  
No Excel 2002 e versões anteriores, o Excel embutido uma cadeia de cálculo para cada planilha em cada pasta de trabalho aberta. Isso resultou em alguma complexidade da maneira links entre planilhas foram tratadas e necessárias algumas cuidado para garantir o recálculo eficiente. Em particular, no Excel 2000, você deve minimizar dependências entre-planilha e planilhas de nome em ordem alfabética para que as folhas que dependem de outras folhas em ordem alfabética vêm após as planilhas que eles dependem.
  
No Excel 2007, a lógica foi aprimorada para habilitar o recálculo em vários segmentos para que não sejam interdependentes de seções da cadeia de cálculo e podem ser calculadas ao mesmo tempo. Você pode configurar o Excel para usar vários threads em um computador de processador único ou um único segmento em um computador com vários processadores ou vários núcleo. 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>Funções (UDFs) definidas pelo usuário assíncrono

Quando um cálculo encontra uma UDF assíncrona, salva o estado da fórmula atual, inicia o UDF e continua a avaliar o restante das células. Quando o cálculo termina avaliando as células aguarda Excel as funções assíncronas concluir se houver funções ainda assíncronas em execução. Como resultados de relatórios cada função assíncrono, Excel termina a fórmula e, em seguida, executa uma nova passagem de cálculo para recalcule em células que usam a célula com a referência para a função assíncrona.
  
## <a name="volatile-and-non-volatile-functions"></a>Funções voláteis e não voláteis

Excel suporta o conceito de uma função volátil, ou seja, uma cujo valor não é assumido para ser o mesmo de um dado momento para o próximo, mesmo se nenhum dos seus argumentos (se levará qualquer) foi alterada. Excel revê células que contêm funções voláteis, juntamente com todos os dependentes, toda vez que for recalcula. Por esse motivo, uma quantidade excessiva a dependência de funções voláteis pode fazer o recálculo tempo lento. Usá-los com moderação.
  
As seguintes funções do Excel são voláteis:
  
- **AGORA**
    
- **HOJE**
    
- **ALEATÓRIOENTRE**
    
- **DESLOCAMENTO**
    
- **INDIRETAS**
    
- **INFO** (dependendo de seus argumentos) 
    
- **CÉLULA** (dependendo de seus argumentos) 
    
- **SOMASE** (dependendo de seus argumentos) 
    
O VBA e a API C suportam maneiras para informar aos Excel que uma função definida pelo usuário (UDF) deve ser tratada como volátil. Usando o VBA, UDF é declarada como volátil, da seguinte maneira.
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

Por padrão, o Excel assume que não sejam voláteis UDFs VBA. Excel apenas aprende que um UDF é volátil quando ela primeiro chama. Um UDF volátil pode ser alterado para não voláteis como no exemplo.
  
Usando a API C, você pode registrar uma função XLL como volátil antes de sua primeira chamada. Ele também permite ativar e desativar o status voláteis de uma função de planilha.
  
Por padrão, o Excel trata XLL UDFs que tem o argumento de intervalo e que são declarados como equivalentes de folha de macro como volátil. Você pode desativar esse estado padrão usando a função de **xlfVolatile** quando o UDF é chamado primeiro. 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>Modos de cálculo, comandos, recálculo seletivo e tabelas de dados

O Excel tem três modos de cálculo:
  
- Automático
    
- Automático, exceto tabelas
    
- Manual
    
Quando o cálculo é definido como automático, o recálculo ocorre depois de cada entrada de dados e determinados eventos, como os exemplos fornecidos na seção anterior. Pastas de trabalho muito grande, o tempo de recálculo pode ser tão longa que os usuários devem limite quando isso acontece, ou seja, recalcular apenas quando eles precisam. Para permitir isso, o Excel oferece suporte para o modo manual. O usuário pode selecionar o modo por meio do sistema de menus do Excel ou programaticamente usando o VBA, COM ou a API C.
  
Tabelas de dados são estruturas especiais em uma planilha. Em primeiro lugar, o usuário configura o cálculo de um resultado em uma planilha. Isso depende de uma ou duas entradas podem ser alteradas principais e outros parâmetros. O usuário, em seguida, pode criar uma tabela dos resultados para um conjunto de valores para uma ou ambas as entradas de chave. A tabela é criada usando o **Assistente de tabela de dados**. Depois que a tabela estiver configurada, o Excel conecta-se as entradas de um a um cálculo e copia o valor resultante para a tabela. Como uma ou duas entradas podem ser usadas, tabelas de dados podem ser uma - ou bidimensional. 
  
Recálculo das tabelas de dados é tratado ligeiramente diferente:
  
- Recálculo é tratado de maneira assíncrona para o recálculo de pasta de trabalho normal para que tabelas grandes podem demorar mais recalcular do resto da pasta de trabalho.
    
- Referências circulares são toleradas. Se o cálculo que é usado para obter o resultado depende de um ou mais valores da tabela de dados, o Excel não retornará um erro quando a dependência circular. 

- Tabelas de dados não use cálculo multithread.
    
Devido a maneira de diferente que Excel manipula o recálculo de tabelas de dados e o fato de que as tabelas grandes que dependem de cálculos de longos ou complexos podem levar muito tempo para calcular, o Excel permite que você desabilite o cálculo automático de tabelas de dados. Para fazer isso, defina o modo de cálculo para automático, exceto tabelas de dados. Quando o cálculo é neste modo, o usuário recalcula as tabelas de dados pressionando F9 ou alguma operação programática equivalente.
  
Excel expõe métodos através do qual você pode alterar o modo de recálculo e controlar o recálculo. Esses métodos foram aprimorados de versão para versão para permitir um controle mais preciso. Os recursos da API C sob este aspecto refletem aqueles que estavam disponíveis no Excel versão 5 e portanto não dê você mesmo controle que você tenha usando o VBA em versões mais recentes. 
  
Usados com mais frequência quando o Excel está no modo de cálculo manual, esses métodos permitem seletivo cálculo dos intervalos, planilhas e pastas de trabalho do recálculo completo de todas as pastas de trabalho abertas e até mesmo completo reconstrução de cadeia de cálculo e a árvore de dependência.
  
### <a name="range-calculation"></a>Cálculo de intervalo

Pressionamento de tecla: nenhum
  
VBA: **intervalo** (introduzida no Excel 2000, alterado no Excel 2007) e **Range.CalculateRowMajorOrder** (introduzida no Excel 2007) 
  
API C: Não suporte
  
- **Modo manual**
    
    Recalcula apenas as células no intervalo determinado independentemente de estarem ou dirty ou não. Comportamento do método **intervalo** alterado no Excel 2007; No entanto, o comportamento antigo ainda é suportado pelo método **Range.CalculateRowMajorOrder** . 
    
- **Modos de automático, exceto tabelas ou automático**
    
    Recalcula a pasta de trabalho, mas não forçar o recálculo do intervalo ou qualquer células do intervalo.
    
### <a name="active-worksheet-calculation"></a>Cálculo da planilha ativa

O pressionamento de tecla: SHIFT + F9
  
VBA: **ActiveSheet.Calculate**
  
API C: **xlcCalculateDocument**
  
- **Todos os modos**
    
    Recalcula as células marcadas para cálculo na planilha ativa.
    
### <a name="specified-worksheet-calculation"></a>Cálculo da planilha especificada

Pressionamento de tecla: nenhum
  
VBA: **planilhas (** referência **). Calcular**
  
API C: Não suporte
  
- **Todos os modos**
    
    Recalcula as células dirty e seus dependentes dentro apenas da planilha especificada. Referência é o nome da planilha como uma cadeia de caracteres ou o número de índice na pasta de trabalho relevante.
    
    Excel 2000 e versões posteriores exponham uma propriedade **Boolean** de planilha, a propriedade **EnableCalculation** . Essa configuração como **True** de **False** dirties todas as células da planilha especificada. Nos modos automáticos, isso também dispara um recálculo da pasta de trabalho inteira. 
    
    No modo manual, o código a seguir faz com que o recálculo da planilha ativa.
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>Árvore de pasta de trabalho reconstruir e forçada recálculo

O pressionamento de tecla: CTRL + ALT + SHIFT + F9 (introduzida no Excel 2002)
  
VBA: **pastas de trabalho (** referência **). ForceFullCalculation** (introduzida no Excel 2007) 
  
API C: Não suporte
  
- **Todos os modos**
    
    Faz com que o Excel para reconstruir a árvore de dependência e a cadeia de cálculo para uma determinada pasta de trabalho e força um recálculo do todas as células que contêm fórmulas.
    
### <a name="all-open-workbooks"></a>Todas as pastas de trabalho

Pressionamento de tecla: F9
  
VBA: **Application. Calculate**
  
API C: **xlcCalculateNow**
  
- **Todos os modos**
    
    Recalcula todas as células que Excel tenha marcado como sujo, ou seja, dependentes da dados voláteis ou alterados e células programaticamente marcadas como sujas. Se o modo de cálculo for automático, exceto tabelas, isso calcula nessas tabelas que requeiram a atualização e também todas as funções voláteis e seus dependentes.
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>Árvore de todas as pastas de trabalho abertas reconstruir e forçada de cálculo

Pressionamento de tecla: CTRL + ALT + F9
  
VBA: **Application.CalculateFull**
  
API C: Não suporte
  
- **Todos os modos**
    
    Recalcula todas as células em pastas de trabalho abertas tudo. Se o modo de cálculo for automático, exceto tabelas, ele força as tabelas a ser recalculado.
    
## <a name="see-also"></a>Confira também



[Recálculo do vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Tipos de dados usados pelo Excel](data-types-used-by-excel.md)
  
[Gerenciamento de memória no Excel](memory-management-in-excel.md)
  
[Excel Programming Concepts](excel-programming-concepts.md)


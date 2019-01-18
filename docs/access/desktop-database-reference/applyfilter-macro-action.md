---
title: Ação da macro AplicarFiltro
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716843"
---
# <a name="applyfilter-macro-action"></a>Ação da macro AplicarFiltro

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **AplicarFiltro** para aplicar um filtro, uma consulta ou uma cláusula SQL WHERE a uma tabela, um formulário ou um relatório para restringir ou classificar os registros da tabela, ou os registros da tabela ou consulta subjacente do formulário ou relatório. Para relatórios, é possível usar esta ação somente em uma macro especificada pela propriedade de evento **AoAbrir** do relatório.

> [!NOTE]
> [!OBSERVAçãO] Você pode usar esta ação para aplicar uma cláusula WHERE do SQL apenas ao aplicar um filtro de servidor. Um filtro de servidor não pode ser aplicado a uma fonte de registros do procedimento armazenado.

## <a name="setting"></a>Configuração

A ação **AplicarFiltro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nome do Filtro</p></td>
<td><p>O nome de um filtro ou uma consulta que restringe ou classifica os registros da tabela, formulário ou relatório. Você pode inserir o nome de uma consulta existente ou um filtro que foi salvo como uma consulta na caixa <strong>Nome do filtro</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do <strong>Construtor de macros</strong> .</p><p><strong>Observação</strong>: quando você estiver usando essa ação para aplicar um filtro de servidor, o argumento Nome do filtro deve estar em branco.</p></td>
</tr>
<tr class="even">
<td><p>Condição Where</p></td>
<td><p>Uma cláusula SQL WHERE válida (sem a palavra WHERE) ou uma expressão que restringe os registros da tabela, do formulário ou do relatório. 

</p>
<p><b>Observação</b>: em uma expressão condição onde argumento, o lado esquerdo da expressão normalmente contém um nome de campo da tabela ou consulta base para o formulário ou relatório. Normalmente, o lado direito da expressão contém os critérios que você deseja aplicar a este campo para restringir ou classificar os registros. Por exemplo, os critérios podem ser o nome de um controle em outro formulário que contém o valor que você deseja que os registros no primeiro formulário devem corresponder. O nome do controle deve ser totalmente qualificado, por exemplo:</p>
<p><strong>Formulários</strong>! <em>formname</em>! <em>controlname</em> Nomes de campo devem ser circundados por aspas duplas e os literais de cadeia de caracteres devem ser circundados por aspas simples. O comprimento máximo do argumento Condição Where é 255 caracteres. Se você precisar inserir uma cláusula SQL WHERE maior, use o método <strong>ApplyFilter</strong> do objeto <strong>DoCmd</strong> no Visual Basic para módulo Applications (VBA). Você pode inserir instruções cláusula SQL WHERE de até 32.768 caracteres no VBA.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Use o argumento Nome do Filtro se você já tiver definido um filtro que forneça os dados apropriados. É possível usar o argumento Condição Onde para inserir diretamente os critérios de restrição. Se você usar ambos os argumentos, o Microsoft Office Access 2007 aplicará a cláusula WHERE aos resultados do filtro. Use um dos argumentos, ou ambos.

## <a name="remarks"></a>Comentários

Você pode aplicar um filtro ou uma consulta a um formulário no modo Formulário ou no modo Folha de Dados.

O filtro e a condição WHERE aplicados tornam-se a configuração da propriedade **Filtrar** ou **ServerFilter** do formulário ou relatório.

Para tabelas e formulários, esta ação é semelhante a clicar em **Aplicar Filtro/Classificar** ou **Aplicar Filtro do Servidor** no menu **Registros**. O comando do menu aplica o filtro criado mais recentemente à tabela ou ao formulário, enquanto a ação **AplicarFiltro** aplica um filtro ou consulta especificado.

Em um banco de dados do Access, se você apontar para **Filtrar** no menu **Registros** e clicar em **Filtrar/Classificar Avançado** após executar a ação **AplicarFiltro**, a janela Filtrar/Classificar Avançado mostrará os critérios de filtragem selecionados com esta ação.

Para remover um filtro e exibir todos os registros de uma tabela ou formulário em um banco de dados do Office Access 2007, você pode usar a ação **MostrarTodosRegistros** ou o comando **Remover Filtro/Classificação** no menu **Registros**. Para remover um filtro em um projeto do Access (.adp), você pode retornar para a janela Filtro do Servidor por Formulário, remover todos os critérios de filtragem e clicar em **Aplicar Filtro do Servidor** no menu **Registros** da barra de ferramentas ou definir a propriedade **ServerFilterByForm** como **False** (0).

Quando você salvar uma tabela ou um formulário, o Access salvará todo filtro definido no momento nesse projeto, mas não aplicará esses filtros automaticamente na próxima vez em que o objeto for aberto (apesar de que aplicará automaticamente qualquer classificação aplicada ao objeto antes de ser salvo). Se desejar aplicar um filtro automaticamente quando um formulário for aberto pela primeira vez, especifique uma macro que contenha a ação **AplicarFiltro** ou um procedimento de evento que contenha o método **ApplyFilter** do objeto **DoCmd** como sendo a configuração da propriedade de evento **AoAbrir** do formulário. Você também pode aplicar um filtro usando a ação **AbrirFormulário** ou **AbrirRelatório** ou seus métodos correspondentes. Para aplicar um filtro automaticamente quando uma tabela for aberta pela primeira vez, você pode abrir a tabela usando uma macro que contenha a ação **AbrirTabela**, seguida imediatamente pela ação **AplicarFiltro**.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação AplicarFiltro para filtrar o formulário de frmFoods conforme ele é aberto.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```




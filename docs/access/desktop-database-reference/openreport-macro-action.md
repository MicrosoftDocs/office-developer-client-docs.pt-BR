---
title: Ação de macro AbrirRelatório
TOCTitle: OpenReport Macro Action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ef2a1f5afd4b8828fdc39744e92d0a4e92ca7bd6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871490"
---
# <a name="openreport-macro-action"></a>Ação de macro AbrirRelatório

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **AbrirRelatório** para abrir um relatório em modo Design ou Visualizar Impressão, ou para enviar o relatório diretamente para a impressora. Também pode restringir os registros impressos no relatório.

## <a name="setting"></a>Configuração

A ação **AbrirRelatório** tem os seguintes argumentos.

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
<td><p>Nome do Relatório</p></td>
<td><p>O nome do relatório a ser aberto. A caixa <strong>Nome do relatório</strong> , na seção <strong>Argumentos da ação</strong> do painel de tarefas do <strong>Construtor de macros</strong> mostra todos os relatórios no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro que contém a ação AbrirRelatório em um banco de dados biblioteca, o Microsoft Access procurará o relatório com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p>Exibir</p></td>
<td><p>O modo de exibição no qual o relatório será aberto. Clique em <strong>Imprimir</strong> (imprimir o relatório imediatamente), <strong>Design</strong> ou <strong>Visualizar Impressão</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Imprimir</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Nome do Filtro</p></td>
<td><p>Um filtro que restringe os registros do relatório. Você pode digitar o nome de uma consulta existente ou de um filtro que foi salvo como consulta. Entretanto, a consulta precisa incluir todos os campos no relatório que você está abrindo ou ter a propriedade <strong>SaídaTodosOsCampos</strong> definida como <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Condição Where</p></td>
<td><p>Uma cláusula SQL WHERE válida (sem a palavra onde) ou expressão que o Access utiliza para selecionar registros do relatório de tabela ou consulta base do. Se você selecionar um filtro com o argumento Nome do filtro, o Access aplica essa cláusula WHERE aos resultados do filtro. Para abrir um relatório e restringir seus registros àqueles especificados pelo valor de um controle em um relatório, use a expressão a seguir:<br />
<strong>[</strong><em>nome_do_campo</em><strong>] = Formulários![</strong><em>nome_do_formulário</em><strong>]![</strong><em>nome do controle em um formulário</em><strong>]</strong><br />
Substitua <em>fieldname</em> pelo nome de um campo na tabela ou consulta do relatório que deseja abrir subjacente. Substitua o nome do formulário e o controle no formulário que contém o valor que você deseja que os registros no relatório para corresponder <em>formname</em> e <em>controlname no formulário</em> .</p>
<p><b>Observação</b>: O comprimento máximo do argumento Condição Where é 255 caracteres. Se você precisar inserir uma cláusula SQL WHERE complexa mais, maior que isso, use o método <b>OpenReport</b> do objeto <b>DoCmd</b> no Visual Basic para módulo Applications (VBA). Você pode inserir instruções cláusula SQL WHERE de até 32.768 caracteres no VBA.</p>
</td>
</tr>
<tr class="odd">
<td><p>Modo Janela</p></td>
<td><p>O modo no qual o relatório será aberta. Clique em <strong>Normal</strong>, <strong>oculto</strong>, <strong>ícone</strong>ou <strong>diálogo</strong> , na caixa <strong>Modo janela</strong> . O padrão é <strong>Normal</strong>.</p>
<p><b>Observação</b>: configurações do modo de janela alguns argumento não se aplicam ao uso de documentos com abas. Para alternar para janelas sobrepostas:
<ol>
<li><p>Click <strong>Options</strong>.</p></li>
<li><p>Na caixa de diálogo <strong>Opções do Access</strong> , clique em <strong>Banco de dados atual</strong>.</p></li>
<li><p>Na seção <strong>Opções do Aplicativo</strong>, em <strong>Opções de Janela de Documento</strong>, clique em <strong>Janelas Sobrepostas</strong>.</p></li>
<li><p>Clique em <strong>Okey</strong>e, em seguida, feche e reabra o banco de dados.</p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A configuração **Imprimir** do argumento **Modo de Exibição** imprime o relatório imediatamente usando as configurações de impressora atuais, sem exibir a caixa de diálogo **Imprimir**. Você também pode usar a ação **AbrirRelatório** para abrir e configurar um relatório e usar a ação Imprimir para imprimi-lo. Por exemplo, convém modificar o relatório ou usar a ação **Imprimir** para alterar as configurações de impressora antes de imprimir.

O filtro e a condição WHERE aplicados se tornam a configuração da propriedade **Filtro** do relatório.

A ação **AbrirRelatório** é semelhante a clicar duas vezes no relatório do Painel de Navegação ou a clicar com o botão direito do mouse no relatório do Painel de Navegação e selecionar um modo de exibição ou o comando **Imprimir**.

> [!TIP] 
> - Para imprimir relatórios semelhantes para diferentes conjuntos de dados, use um filtro ou uma cláusula WHERE para restringir os registros impressos no relatório. Edite a macro para aplicar um filtro diferente ou altere o argumento Condição Onde.
> 
> - Você pode arrastar um relatório do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirRelatório** que abre o relatório em modo Relatório.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação AbrirRelatório para passar um parâmetro que filtra um relatório conforme ele é aberto. O relatório de **rptChapters** exibe os registros para o autor especificado, passando-se o item selecionado na caixa de combinação **cboAuthors** para o parâmetro SelectedAuthor.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```

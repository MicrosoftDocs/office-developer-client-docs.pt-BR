---
title: Ação da macro AbrirRelatório
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288347"
---
# <a name="openreport-macro-action"></a>Ação da macro AbrirRelatório

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **AbrirRelatório** para abrir um relatório em modo Design ou Visualizar Impressão, ou para enviar o relatório diretamente para a impressora. Também pode restringir os registros impressos no relatório.

## <a name="setting"></a>Setting

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
<td><p>Nome do relatório</p></td>
<td><p>O nome do relatório que será aberto. A <strong>caixa Nome do</strong> Relatório na seção <strong>Argumentos da</strong> Ação do painel Construtor de <strong>Macros</strong> mostra todos os relatórios no banco de dados atual. Esse é um argumento obrigatório. Se você executar uma macro que contém a ação AbrirRelatório em um banco de dados biblioteca, o Microsoft Access procurará o relatório com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
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
<td><p>Uma cláusula SQL WHERE  (sem a palavra WHERE) válida ou expressão que o Access usa para selecionar registros da tabela ou consulta subjacente do relatório. Se você selecionar um filtro com o argumento Nome do Filtro, o Access aplicará essa cláusula WHERE aos resultados do filtro. Para abrir um relatório e restringir seus registros àqueles especificados pelo valor de um controle em um relatório, use a expressão a seguir:<br />
<strong>[</strong><em>nome_do_campo</em><strong>] = Formulários![</strong><em>nome_do_formulário</em><strong>]![</strong><em>nome do controle em um formulário</em><strong>]</strong><br />
Substitua <em>nome_do_campo</em> pelo nome de um campo na tabela ou consulta subjacente do relatório que será aberto. Substitua <em>o nome do</em> formulário e o nome do controle no formulário pelo nome do formulário e o controle no formulário que contém o valor que você deseja que os registros do relatório sejam igualmente. <em></em></p>
<p><b>OBSERVAÇÃO:</b>o comprimento máximo do argumento Condição Where é de 255 caracteres. Se você precisar inserir uma cláusula SQL WHERE mais complexa e extensa do que essa, use o método <b>OpenReport</b> do objeto <b>DoCmd</b> em um módulo do VBA (Visual Basic for Applications). É possível inserir instruções de cláusulas SQL WHERE de até 32.768 caracteres no VBA.</p>
</td>
</tr>
<tr class="odd">
<td><p>Modo Janela</p></td>
<td><p>O modo no qual o relatório será aberto. Clique <strong>em Normal</strong>, <strong>Oculto</strong>, <strong>Ícone</strong>ou <strong>Caixa de</strong> Diálogo na caixa Modo <strong>janela.</strong> O padrão é <strong>Normal</strong>.</p>
<p><b>OBSERVAÇÃO:</b>algumas configurações de argumento do Modo Janela não se aplicam ao usar documentos com guias. Para alternar para janelas sobrepostas:
<ol>
<li><p>Clique em <strong>Opções</strong>.</p></li>
<li><p>Na caixa de diálogo <strong>Opções do Access</strong>, clique em <strong>Banco de Dados Atual</strong>.</p></li>
<li><p>Na seção <strong>Opções do Aplicativo</strong>, em <strong>Opções de Janela de Documento</strong>, clique em <strong>Janelas Sobrepostas</strong>.</p></li>
<li><p>Clique <strong>em OK</strong>e feche e reabra o banco de dados.</p></li>
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

O exemplo a seguir mostra como usar a ação Abrir Relatório para passar um parâmetro que filtra um relatório à medida que ele é aberto. O **relatório rptChapters** exibe os registros do autor especificado passando o item selecionado na caixa de combinação **cboAuthors** para o parâmetro SelectedAuthor.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

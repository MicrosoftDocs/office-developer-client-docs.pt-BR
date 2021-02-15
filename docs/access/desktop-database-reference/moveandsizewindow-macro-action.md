---
title: Ação da macro MovereDimensionarJanela
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288803"
---
# <a name="moveandsizewindow-macro-action"></a>Ação da macro MovereDimensionarJanela

**Aplica-se ao:** Access 2013, Office 2013

Se você definiu suas opções de janela de documento para usar janelas sobrepostas em vez de documentos com guias, você pode usar a ação **MoveAndSizeWindow** para mover ou resize a janela ativa. Para obter informações sobre como definir opções de janela de documento, consulte a seção Comentários.

## <a name="setting"></a>Setting

A **ação MoveAndSizeWindow** tem os seguintes argumentos.

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
<td><p><strong>Right</strong></p></td>
<td><p>A nova posição horizontal do canto superior esquerdo da janela, medida a partir da extremidade esquerda da janela. Insira a posição na caixa <strong>Direita</strong> na seção <strong>Argumentos da</strong> Ação do painel Construtor de Macros.</p></td>
</tr>
<tr class="even">
<td><p><strong>Down</strong></p></td>
<td><p>A nova posição vertical do canto superior esquerdo da janela, medida a partir da extremidade superior da janela.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Width</strong></p></td>
<td><p>A nova largura da janela.</p></td>
</tr>
<tr class="even">
<td><p><strong>Height</strong></p></td>
<td><p>A nova altura da janela.</p></td>
</tr>
</tbody>
</table>


Se você deixar um argumento em branco, o Microsoft Access usará a configuração atual da janela.

Você deve inserir um valor para pelo menos um argumento.

> [!NOTE]
> Cada medida está em polegadas ou centímetros, dependendo das configurações regionais no Painel de Controle do Windows.

## <a name="remarks"></a>Comentários

Para configurar um aplicativo para usar janelas sobrepostas em vez de documentos com guias, use o seguinte procedimento:

1.  Opções de **clique**

2.  Clique em **Banco de Dados Atual.**

3.  Na seção **Opções do Aplicativo**, em **Opções de Janela de Documento**, clique em **Janelas Sobrepostas**.

4.  Clique **em OK** e feche e reabra o banco de dados.

Esta ação é semelhante a clicar em **Mover** **ou Tamanho** no menu Controle **da** janela. Com os comandos do menu, você usa as teclas de seta do teclado para mover ou resize a janela. Com a **ação MoveAndSizeWindow,** insira as medições de posição e tamanho diretamente. Você também pode usar o mouse para mover e tamanho de janelas.

Você pode usar essa ação em qualquer janela, em qualquer exibição.

> [!TIP]
> - Para mover uma janela sem re tamanho, insira valores para os argumentos **Right** e **Down,** mas deixe os argumentos **Width** e **Height** em branco.
> - Para re tamanho de uma janela sem movimentação, insira valores para os argumentos **Width** e **Height,** mas deixe os argumentos **Right** e **Down** em branco.

Para executar a **ação MoveAndSizeWindow** em um módulo do VBA (Visual Basic for Applications), use o método **MoveSize** do objeto **DoCmd.**

## <a name="example"></a>Exemplo

**Sincronizar formulários usando uma macro**

A macro a seguir abre um formulário de Lista de Produtos no canto inferior direito do formulário Fornecedores, exibindo os produtos do fornecedor atual. Ele mostra o uso das ações **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm** e **MoveAndSizeWindow.** Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl** e **StopMacro.** Essa macro deve ser anexada ao botão Revisar Produtos no formulário Fornecedores.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On</strong>: <strong>No</strong></p></td>
<td><p>Interrompe a atualização de tela quando a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([ID do fornecedor])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>vá para o registro do fornecedor cujos produtos você deseja ver e clique no botão Revisar Produtos novamente. <strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</p></td>
<td><p>Se não houver fornecedor atual no formulário Fornecedores, exibe uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CompanyName</p></td>
<td><p>Mova o foco para o controle CompanyName.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Pare a macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: Exibição de Lista <strong>de</strong>Produtos : <strong>Nome do Filtro de</strong>Folha de Dados : <strong>Condição</strong>Onde : [ID do fornecedor] = [Formulários]! [Fornecedores]! [SupplierID] <strong>Modo de Dados</strong>: <strong>Ler Modo Somente Janela</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário Lista de Produtos e mostre os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>À</strong>direita: 0,7799 &quot; <strong>para baixo:</strong>1,8&quot;</p></td>
<td><p>Posiciona o formulário Lista de Produtos no canto inferior direito do formulário Fornecedores.</p></td>
</tr>
</tbody>
</table>


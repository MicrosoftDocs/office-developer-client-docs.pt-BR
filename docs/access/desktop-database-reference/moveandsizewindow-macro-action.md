---
title: Ação de Macro Moveredimensionarjanela
TOCTitle: MoveAndSizeWindow Macro Action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d423668f5ef53abf4216fa8f976c674474a752ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463925"
---
# <a name="moveandsizewindow-macro-action"></a>Ação de Macro Moveredimensionarjanela


**Aplica-se a**: Access 2013 | Office 2013


Se você tiver configurado as opções de janela para usar janelas sobrepostas, em vez de documentos com guias para seu documento, você pode usar a ação **Moveredimensionarjanela** para mover ou redimensionar a janela ativa. Para obter informações sobre como configurar opções da janela de documento, consulte a seção comentários.

## <a name="setting"></a>Configuração

A ação **Moveredimensionarjanela** tem os seguintes argumentos.

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
<td><p>A nova posição horizontal do canto superior esquerdo da janela, medida a partir da extremidade esquerda da janela. Insira a posição na caixa <strong>direita</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</p></td>
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


Se você deixar um argumento em branco, o Microsoft Access usa a configuração atual da janela.

Você deve inserir um valor para pelo menos um argumento.


> [!NOTE]
> <P>Cada medida está em polegadas ou centímetros, dependendo das configurações regionais no painel de controle do Windows.</P>



## <a name="remarks"></a>Comentários

Para configurar um aplicativo para usar janelas sobrepostas, em vez de documentos com guias, use o procedimento a seguir:

1.  e, em seguida, clique em **Opções**

2.  Clique em **banco de dados atual**.

3.  Na seção **Opções do Aplicativo**, em **Opções de Janela de Documento**, clique em **Janelas Sobrepostas**.

4.  Clique em **Okey**e, em seguida, feche e reabra o banco de dados.

Esta ação é semelhante a clicar em **Mover** ou **Dimensionar** , no menu **controle** da janela. Com os comandos de menu, você pode usar teclas de direção do teclado para mover ou redimensionar a janela. Com a ação **Moveredimensionarjanela** , insira as medidas de tamanho e posição diretamente. Você também pode usar o mouse para mover e dimensionar janelas.

Você pode usar essa ação em qualquer janela, em qualquer modo de exibição.

**Dicas**

  - Para mover uma janela sem redimensioná-la, insira valores para a **direita** e **para baixo** argumentos, mas deixar os argumentos **largura** e **Altura** em branco.

  - Para redimensionar uma janela sem movê-lo, insira valores para a **largura** e **Altura** argumentos, mas deixar os argumentos **direita** e **para baixo** em branco.

Para executar a ação **Moveredimensionarjanela** em um módulo Visual Basic for Applications (VBA), use o método **MoveSize** do objeto **DoCmd** .

## <a name="example"></a>Exemplo

**Sincronizar formulários usando uma macro**

A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações. Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** . Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condição</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Eco no</strong>: <strong>não</strong></p></td>
<td><p>Pare a atualização da tela enquanto a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p>ÉNulo ([ID do fornecedor])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente. <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</p></td>
<td><p>Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: NomeDaEmpresa</p></td>
<td><p>Mova o foco para o controle NomeDaEmpresa.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Interrompa a macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [código do fornecedor] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Moveredimensionarjanela</strong></p></td>
<td><p><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</p></td>
<td><p>Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</p></td>
</tr>
</tbody>
</table>


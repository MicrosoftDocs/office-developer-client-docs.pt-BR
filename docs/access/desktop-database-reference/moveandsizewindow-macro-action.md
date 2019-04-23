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

Se você tiver definido as opções de janela de documento para usar janelas sobrepostas em vez de documentos com guias, poderá usar a ação **moveredimensionarjanela** para mover ou redimensionar a janela ativa. Para obter informações sobre como definir as opções de janela de documento, consulte a seção comentários.

## <a name="setting"></a>Configuração

A ação **moveredimensionarjanela** tem os seguintes argumentos.

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
<td><p>A nova posição horizontal do canto superior esquerdo da janela, medida a partir da extremidade esquerda da janela. Insira a posição na caixa <strong>à direita</strong> na seção <strong>argumentos da ação</strong> do painel Construtor de macros.</p></td>
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
> Cada medida é em polegadas ou centímetros, dependendo das configurações regionais no painel de controle do Windows.

## <a name="remarks"></a>Comentários

Para configurar um aplicativo para usar janelas sobrepostas em vez de documentos com guias, use o seguinte procedimento:

1.  **Opções** de clique

2.  Clique em **banco de dados atual**.

3.  Na seção **Opções do Aplicativo**, em **Opções de Janela de Documento**, clique em **Janelas Sobrepostas**.

4.  Clique em **OK**e feche e reabra o banco de dados.

Esta ação é semelhante a clicar em **mover** ou **dimensionar** no menu **controle** da janela. Com os comandos de menu, você usa as teclas de seta do teclado para mover ou redimensionar a janela. Com a ação **moveredimensionarjanela** , você insere as medidas de posição e de tamanho diretamente. Você também pode usar o mouse para mover e dimensionar janelas.

Você pode usar essa ação em qualquer janela, em qualquer modo de exibição.

> [!TIP]
> - Para mover uma janela sem redimensioná-la, insira valores para os argumentos **Right** e **down** , mas deixe os argumentos **Width** e **Height** em branco.
> - Para redimensionar uma janela sem movê-la, insira valores para os argumentos **Width** e **Height** , mas deixe os argumentos **Right** e **down** em branco.

Para executar a ação **moveredimensionarjanela** em um módulo do VBA (Visual Basic for Applications), use o método **MoverDimensionar** do objeto **DoCmd** .

## <a name="example"></a>Exemplo

**Sincronizar formulários usando uma macro**

A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso das ações **eco**, **MessageBox**, **IrParaControle**, **PararMacro**, **AbrirFormulário**e **moveredimensionarjanela** . Também mostra o uso de uma expressão condicional com as ações **MessageBox**, **IrParaControle**e **PararMacro** . Essa macro deve ser anexada ao botão reVisar produtos no formulário fornecedores.

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
<td><p><strong>Echo ativado</strong>: <strong>não</strong></p></td>
<td><p>Interrompa a atualização da tela enquanto a macro estiver em execução.</p></td>
</tr>
<tr class="even">
<td><p>Énulo ([código do fornecedor])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: mova para o registro de fornecedor cujos produtos você deseja ver e, em seguida, clique no botão revisar produtos novamente. <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecionar um fornecedor</p></td>
<td><p>Se não houver um fornecedor atual no formulário fornecedores, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CompanyName</p></td>
<td><p>Mover o foco para o controle CompanyName.</p></td>
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
<td><p><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>de lista de produtos: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [CódigoDoFornecedor ID] = [formulários]! [Fornecedores]! [CódigoDoFornecedor] <strong>Modo de dados</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>normal</strong></p></td>
<td><p>Abra o formulário lista de produtos e mostre os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Moveredimensionarjanela</strong></p></td>
<td><p><strong>direita</strong>: 0,7799&quot; <strong>baixo</strong>: 1,8&quot;</p></td>
<td><p>Posicione o formulário lista de produtos no canto inferior direito do formulário fornecedores.</p></td>
</tr>
</tbody>
</table>


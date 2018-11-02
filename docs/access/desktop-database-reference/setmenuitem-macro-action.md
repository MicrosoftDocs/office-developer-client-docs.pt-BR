---
title: Ação da macro DefinirItemDoMenu
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ecdfcb638a471a91cc6249636748c02b341151b8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922549"
---
# <a name="setmenuitem-macro-action"></a>Ação da macro DefinirItemDoMenu


**Aplica-se a**: Access 2013, o Office 2013

Use a ação **DefinirItemDoMenu** para definir o estado de itens de menu (habilitado ou desabilitado, selecionado ou não selecionado) em menus personalizados ou globais, na guia **Suplementos**.


> [!NOTE]
> <P>[!OBSERVAçãO] A ação <STRONG>DefinirItemDoMenu</STRONG> funciona somente com menus personalizados e globais criados por macros de menu. A ação <STRONG>DefinirItemDoMenu</STRONG> está incluída no Microsoft Access somente para fins de compatibilidade com versões anteriores. Ela não funciona com a funcionalidade da barra de comandos, No entanto, você pode usar as propriedades <STRONG>Habilitado</STRONG> e <STRONG>Estado</STRONG> em um módulo do VBA (Visual Basic for Applications) para habilitar ou desabilitar e selecionar ou cancelar a seleção de itens em menus de atalho ou em menus personalizados ou globais.</P>



## <a name="setting"></a>Configuração

A ação **DefinirItemDoMenu** tem os seguintes argumentos.

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
<td><p><strong>Índice de menu</strong></p></td>
<td><p>O índice do menu que contém o comando para o qual você deseja definir o estado. Insira um valor inteiro, começando com 0, para o índice do menu desejado no menu personalizado ou global. Insira o valor de índice na caixa de <strong>Índice de Menu</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros. O índice está em relação à posição do menu da macro do menu para o menu personalizado ou global (a posição desta ação <strong>AdicionarMenu</strong> da macro do menu, contado a partir de 0). A exibição do menu pode ser um pouco diferente, porque você pode usar expressões condicionais da macro do menu para ocultar ou exibir itens de menu personalizado. Este é um argumento obrigatório. Se você seleciona um menu com este argumento e deixar os argumentos <strong>Índice de comando</strong> e <strong>Índice de subcomando</strong> em branco, é possível habilitar ou desabilitar o nome do menu propriamente dito. No entanto, você não pode selecionar ou desmarcar um nome de menu (o Access ignora as configurações da <strong>seleção</strong> e <strong>desmarque o</strong> do argumento <strong>sinalizador</strong> para nomes de menu).</p></td>
</tr>
<tr class="even">
<td><p><strong>Índice de comando</strong></p></td>
<td><p>O índice do comando para o qual você deseja definir o estado. Insira um valor inteiro, começando em 0, para o índice do comando desejado no menu selecionado pelo argumento <strong>Índice de menu</strong>. O índice é relativo à posição do comando no grupo de macros que define o menu selecionado do menu personalizado ou global (a posição da macro desse comando no grupo de macros, contando de 0). A exibição do menu pode ser ligeiramente diferente, porque você pode usar expressões condicionais no grupo de macros do menu para ocultar ou exibir os comandos do menu personalizado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Índice de subcomando</strong></p></td>
<td><p>O índice do subcomando para o qual você deseja definir o estado. Isso só será aplicável se o comando desejado tiver um submenu. Insira um valor inteiro, começando em 0, para o índice do subcomando desejado no submenu selecionado pelo argumento <strong>Índice de comando</strong>. O índice é relativo à posição do subcomando no grupo de macros que define o submenu selecionado do menu personalizado ou global (a posição da macro desse subcomando no grupo de macros, contando de 0).</p></td>
</tr>
<tr class="even">
<td><p><strong>Flag</strong></p></td>
<td><p>O estado para o qual você deseja definir o comando ou o subcomando. Clique em <strong>Cinza</strong> (para desabilitar o comando — ele ficará esmaecido), em <strong>Anular Cinza</strong> (para habilitá-lo), em <strong>Marcar</strong> (para colocar uma marca no comando — geralmente indicando que ele foi selecionado ou alternado) ou em <strong>Desmarcar</strong> (para remover a marca). O padrão é <strong>Anular Cinza</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **DefinirItemDoMenu** funciona somente em um menu personalizado ou global. Se a janela ativa não tiver um menu personalizado ou global, a execução de uma macro contendo a ação **DefinirItemDoMenu** causará um erro em tempo de execução.

Você pode usar essa ação para definir o estado de comandos e subcomandos de menu, mas não de subcomandos de subcomandos.

Para executar a ação **DefinirItemDoMenu** em um módulo do VBA (Visual Basic for Applications), use o método **SetMenuItem** do objeto **DoCmd**.


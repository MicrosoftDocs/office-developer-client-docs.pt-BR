---
title: Ação de macro ExcluirObjeto
TOCTitle: DeleteObject Macro Action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 85e9fc888e06a69be6f458ed03ad92b8253b30a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463465"
---
# <a name="deleteobject-macro-action"></a>Ação de macro ExcluirObjeto


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **ExcluirObjeto** para excluir um objeto de banco de dados especificado.


> [!NOTE]
> <P>[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</P>



## <a name="setting"></a>Configuração

A ação **ExcluirObjeto** tem os seguintes argumentos.

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
<td><p><strong>Tipo de Objeto</strong></p></td>
<td><p>O tipo de objeto que será excluído. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Para excluir o objeto selecionado no Painel de Navegação, deixe este argumento em branco.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nome do Objeto</strong></p></td>
<td><p>O nome do objeto a ser excluído. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>. Se você deixar a caixa <strong>Tipo de objeto</strong> , deixe esta caixa em branco também. Se você executar uma macro que contém a ação <strong>ExcluirObjeto</strong> em um banco de dados biblioteca, o Microsoft Office Access 2007 primeiro procurará o objeto com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
</tbody>
</table>



> [!WARNING]
> <P>[!CUIDADO] Se você deixar as caixas <STRONG>Tipo de Objeto</STRONG> e <STRONG>Nome do Objeto</STRONG> em branco, o Access excluirá o objeto selecionado no Painel de Navegação sem exibir uma mensagem de aviso ao encontrar a ação <STRONG>ExcluirObjeto</STRONG>.</P>



## <a name="remarks"></a>Comentários

Você pode usar a ação **ExcluirObjeto** para excluir objetos temporários criados ao executar a macro. Por exemplo, é possível usar a ação **AbrirConsulta** para executar uma consulta criar tabela que cria uma tabela temporária. Quando tiver concluído o uso da tabela temporária, você poderá usar a ação **ExcluirObjeto** para excluí-la.

Esta ação equivale a selecionar um objeto no Painel de Navegação e pressionar a tecla DELETE ou clicar com o botão direito do mouse no objeto no Painel de Navegação e clicar em **Excluir**.

Para executar a ação **ExcluirObjeto** em um módulo do Visual Basic for Applications, use o método **DeleteObject** do objeto **DoCmd**.


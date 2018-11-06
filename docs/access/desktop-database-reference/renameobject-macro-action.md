---
title: Ação da macro RenomearObjeto
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7d47a59bc82cb6f603fc52d45c675eb8e2877f91
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998963"
---
# <a name="renameobject-macro-action"></a>Ação da macro RenomearObjeto

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **RenomearObjeto** para renomear um objeto de banco de dados especificado.

> [!NOTE]
> [!OBSERVAçãO] This action will not be allowed if the database is not trusted.

## <a name="setting"></a>Configuração

A ação **RenomearObjeto** tem os seguintes argumentos.

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
<td><p><strong>Novo nome</strong></p></td>
<td><p>Um novo nome para o objeto de banco de dados. Digite o nome do objeto na caixa <strong>Novo Nome</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Este é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo de Objeto</strong></p></td>
<td><p>O tipo de objeto a ser renomeado. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong>. Para renomear o objeto selecionado no Painel de Navegação, deixe esse argumento em branco.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nome antigo</strong></p></td>
<td><p>O nome do objeto a ser renomeado. A caixa <strong>Nome Antigo</strong> mostra todos os objetos de banco de dados do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>. Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, faça o mesmo com este argumento. 

</p><p><strong>Observação</strong>: se você executar uma macro que contém a ação <STRONG>Renomear</STRONG> um banco de dados biblioteca, o Microsoft Access procurará primeiro para o objeto com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O novo nome do objeto de banco de dados deve cumprir as convenções de nomeação padrão para objetos do Access.

Não é possível renomear um objeto aberto.

Se você deixar em branco os argumentos **Tipo de Objeto** e **Nome Antigo**, o Access renomeará o objeto selecionado no Painel de Navegação. Para selecionar um objeto nesse painel, você pode usar a ação **SelecionarObjeto** com o argumento **No Painel de Navegação** definido como **Sim**.

Outra maneira de renomear um objeto é clicar com o botão direito do mouse no Painel de Navegação, clicar em **Renomear** e digitar um novo nome. Com a ação **RenomearObjeto**, você não precisa selecionar primeiro o objeto no Painel de Navegação nem interromper a macro para digitar o novo nome.

Essa ação é diferente da ação **CopiarObjeto**, que cria uma cópia do objeto com um novo nome.

Para executar a ação **RenomearObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **Renomear** do objeto **DoCmd**.


---
title: Ação de macro AbrirModoDeExibição
TOCTitle: OpenView Macro Action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ee0a46e909c86534693638de98f42980bccfebba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870167"
---
# <a name="openview-macro-action"></a>Ação de macro AbrirModoDeExibição


**Aplica-se a**: Access 2013, o Office 2013

Em um projeto do Access, você pode usar a ação **AbrirModoDeExibição** para abrir um modo de exibição em modo Folha de Dados, modo Design ou Visualizar Impressão. Esta ação executa o modo de exibição nomeado quando aberta em modo Folha de Dados. É possível selecionar a entrada de dados do modo de exibição e restringir os registros exibidos pelo modo de exibição.


> [!NOTE]
> <P>[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</P>



## <a name="setting"></a>Configuração

A ação **AbrirModoDeExibição** tem os seguintes argumentos.

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
<td><p><strong>Nome do Modo de Exibição</strong></p></td>
<td><p>O nome da exibição a ser aberto. A caixa de <strong>Nome de exibição</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os modos de exibição no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirModoDeExibição</strong> em um banco de dados biblioteca, o Microsoft Access procurará o modo de exibição com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual o modo de exibição será aberto. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados do modo de exibição. Isso se aplica somente a modos de exibição abertos no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes em um modo de exibição do Painel de Navegação ou a clicar com o botão direito do mouse no modo de exibição do Painel de Navegação e clicar no comando desejado.

**Dicas**

  - Você pode arrastar um modo de exibição do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirModoDeExibição** que abre o modo de exibição em modo Folha de Dados.

  - Se você não deseja exibir as mensagens do sistema que normalmente aparecem quando um modo de exibição é executado (indicando que é um modo de exibição ou mostrando quantos registros serão afetados), use a ação **DefinirAviso** para suprimir a exibição dessas mensagens.

Para executar a ação **AbrirModoDeExibição** em um módulo do VBA (Visual Basic for Applications), use o método **OpenView** do objeto **DoCmd**.


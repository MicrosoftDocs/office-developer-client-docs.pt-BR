---
title: Ação de macro AbrirTabela
TOCTitle: OpenTable Macro Action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 729c1f14d49b3f80ec6307ce775066d3291b96de
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463822"
---
# <a name="opentable-macro-action"></a>Ação de macro AbrirTabela


**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **AbrirTabela** para abrir uma tabela em modo Folha de Dados, modo Design ou Visualizar Impressão. Também pode selecionar um modo de entrada de dados para a tabela.

## <a name="setting"></a>Configuração

A ação **AbrirTabela** tem os seguintes argumentos.

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
<td><p><strong>Nome da Tabela</strong></p></td>
<td><p>O nome da tabela para abrir. Caixa <strong>Nome da tabela</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todas as tabelas no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirTabela</strong> em um banco de dados biblioteca, o Microsoft Access procurará a tabela com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual a tabela será aberta. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados da tabela. Isso se aplica somente às tabelas abertas em modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes em uma tabela do Painel de Navegação ou a clicar com o botão direito do mouse na tabela do Painel de Navegação e selecionar um modo de exibição.


> [!TIP]
> <P>[!DICA] Você pode arrastar uma tabela do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação <STRONG>AbrirTabela</STRONG> que abre a tabela em modo Folha de Dados.</P>



Para executar a ação **AbrirTabela** em um módulo do VBA (Visual Basic for Applications), use o método **OpenTable** do objeto **DoCmd**.


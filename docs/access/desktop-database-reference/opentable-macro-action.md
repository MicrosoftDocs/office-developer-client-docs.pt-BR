---
title: Ação da macro AbrirTabela
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288291"
---
# <a name="opentable-macro-action"></a>Ação da macro AbrirTabela

**Aplica-se ao:** Access 2013, Office 2013

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
<td><p>O nome da tabela que será aberta. A caixa <strong>Nome da Tabela</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros mostra todas as tabelas do banco de dados atual. Esse é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirTabela</strong> em um banco de dados biblioteca, o Microsoft Access procurará a tabela com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
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
> [!DICA] Você pode arrastar uma tabela do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirTabela** que abre a tabela em modo Folha de Dados.

Para executar a ação **AbrirTabela** em um módulo do VBA (Visual Basic for Applications), use o método **OpenTable** do objeto **DoCmd**.


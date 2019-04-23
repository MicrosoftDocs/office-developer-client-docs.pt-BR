---
title: Ação da macro AbrirModoDeExibição
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 88bebab46cd6b76fb101c86c4fe33c5ab86a3e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288298"
---
# <a name="openview-macro-action"></a>Ação da macro AbrirModoDeExibição

**Aplica-se ao:** Access 2013, Office 2013

Em um projeto do Access, você pode usar a ação **AbrirModoDeExibição** para abrir um modo de exibição em modo Folha de Dados, modo Design ou Visualizar Impressão. Esta ação executa o modo de exibição nomeado quando aberta em modo Folha de Dados. É possível selecionar a entrada de dados do modo de exibição e restringir os registros exibidos pelo modo de exibição.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

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
<td><p>O nome do modo de exibição que será aberto. A caixa <strong>nome do modo de exibição</strong> na seção argumentos da <strong>ação</strong> do painel Construtor de macros mostra todos os modos de exibição no banco de dados atual. Esse é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirModoDeExibição</strong> em um banco de dados biblioteca, o Microsoft Access procurará o modo de exibição com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
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

> [!TIP]
> - Você pode arrastar um modo de exibição do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirModoDeExibição** que abre o modo de exibição em modo Folha de Dados.
> - Se você não deseja exibir as mensagens do sistema que normalmente aparecem quando um modo de exibição é executado (indicando que é um modo de exibição ou mostrando quantos registros serão afetados), use a ação **DefinirAviso** para suprimir a exibição dessas mensagens.

Para executar a ação **AbrirModoDeExibição** em um módulo do VBA (Visual Basic for Applications), use o método **OpenView** do objeto **DoCmd**.


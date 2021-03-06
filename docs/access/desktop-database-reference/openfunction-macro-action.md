---
title: Ação da macro AbrirFunção
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b13d21ef1bd8a95587eb78cd448f19f9fd0c24c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288361"
---
# <a name="openfunction-macro-action"></a>Ação da macro AbrirFunção

**Aplica-se ao:** Access 2013, Office 2013

Em um projeto do Access, você pode usar a ação **AbrirFunção** para abrir uma função definida pelo usuário no modo Folha de Dados, uma função in-line no modo Design, o modo Editor de Texto do SQL (para uma função definida pelo usuário escalar ou de tabela) ou Visualizar Impressão. Esta ação executa a função definida pelo usuário quando aberta em modo Folha de Dados. Você também pode selecionar o modo de entrada de dados para a função definida pelo usuário e restringir os registros exibidos pela função definida pelo usuário.

> [!NOTE]
> Essa ação não será permitida se o banco de dados não for confiável. 

## <a name="setting"></a>Setting

A ação **AbrirFunção** tem os seguintes argumentos.

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
<td><p><strong>Nome da função</strong></p></td>
<td><p>O nome da função definida pelo usuário que será aberta. A caixa <strong>Nome da Função</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros mostra todas as funções definidas pelo usuário no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>Function</strong> em um banco de dados biblioteca, o Microsoft Access primeiro procura a função com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual a função definida pelo usuário será aberta. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados da função definida pelo usuário. Isso se aplica somente a funções definidas pelo usuário abertas no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes em uma função definida pelo usuário do Painel de Navegação ou a clicar com o botão direito do mouse na função do Painel de Navegação e selecionar um modo de exibição.

Alternar para o modo Design enquanto a função definida pelo usuário é aberta remove a configuração do argumento **Modo de Dados** da função definida pelo usuário. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.

> [!TIP]
> - Você pode selecionar uma função definida pelo usuário no Painel de Navegação e arrastá-la para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirFunção** que abre a função definida pelo usuário em modo Folha de Dados.
> - Se você não desejar exibir as mensagens de sistema que normalmente aparecem quando uma função definida pelo usuário é executada (indicando que é uma função definida pelo usuário e mostrando quantos registros serão afetados), poderá usar a ação **DefinirAvisos** para suprimir a exibição dessas mensagens.

Para executar a ação **AbrirFunção** em um módulo do VBA (Visual Basic for Applications), use o método **OpenFunction** do objeto **DoCmd**.


---
title: Ação da macro AbrirConsulta
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3294efe5ea1ab0f82be19f5c64a51287cc4df9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288340"
---
# <a name="openquery-macro-action"></a>Ação da macro AbrirConsulta

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **AbrirConsulta** para abrir uma consulta de seleção ou tabela de referência cruzada em modo Folha de Dados, modo Design ou Visualizar Impressão. Esta ação executa uma consulta de ação. Também é possível selecionar um modo de entrada de dados para a consulta.

> [!NOTE]
> [!OBSERVAçãO] Esta ação só está disponível no ambiente de banco de dados do Access (.mdb ou .accdb). Consulte as ações **AbrirModoDeExibição**, **AbrirProcedimentoArmazenado** ou **AbrirFunção** se estiver usando o ambiente de the projeto do Access (.adp).

## <a name="setting"></a>Setting

A ação **AbrirConsulta** tem os seguintes argumentos.

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
<td><p><strong>Nome da Consulta</strong></p></td>
<td><p>O nome da consulta que será aberta. A <strong>caixa Nome da Consulta</strong> na seção <strong>Argumentos</strong> da Ação do painel Construtor de Macros mostra todas as consultas no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro contendo a ação <strong>OpenQuery</strong> em um banco de dados biblioteca, o Microsoft Access primeiro procura a consulta com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual a consulta será aberta. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados da consulta. Isso se aplica somente às consultas abertas em modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se você usar **Folha de Dados** para o argumento **Modo de Exibição**, o Access exibirá o conjunto de resultados se a consulta for uma consulta de seleção, tabela de referência cruzada, união ou passagem cuja propriedade **RetornarRegistros** esteja definida como **Sim**; e executará a consulta se for uma consulta de ação, definição de dados ou passagem cuja propriedade **RetornarRegistros** esteja definida como **Não**.

A ação **AbrirConsulta** é semelhante a clicar duas vezes na consulta do Painel de Navegação ou a clicar com o botão direito do mouse na consulta do Painel de Navegação e selecionar um modo de exibição. Com esta ação, é possível selecionar outras opções.

> [!TIP]
> - Você pode arrastar uma consulta do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirConsulta** que abre a consulta em modo Folha de Dados. Alternar para o modo Design enquanto a consulta é aberta remove a configuração do argumento **Modo de Dados** da consulta. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.
> - Se você não desejar exibir as mensagens de sistema que normalmente aparecem quando uma consulta de ação é executada (indicando que é uma consulta de ação e mostrando quantos registros serão afetados), poderá usar a ação **DefinirAvisos** para suprimir a exibição dessas mensagens.

Para executar a ação **AbrirConsulta** em um módulo do VBA (Visual Basic for Applications), use o método **OpenQuery** do objeto **DoCmd**.


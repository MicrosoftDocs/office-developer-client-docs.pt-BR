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
ms.openlocfilehash: fe08f6c6ab0eba46f7fff2713403f56e82983357
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999061"
---
# <a name="openquery-macro-action"></a>Ação da macro AbrirConsulta

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **AbrirConsulta** para abrir uma consulta de seleção ou tabela de referência cruzada em modo Folha de Dados, modo Design ou Visualizar Impressão. Esta ação executa uma consulta de ação. Também é possível selecionar um modo de entrada de dados para a consulta.

> [!NOTE]
> [!OBSERVAçãO] Esta ação só está disponível no ambiente de banco de dados do Access (.mdb ou .accdb). Consulte as ações **AbrirModoDeExibição**, **AbrirProcedimentoArmazenado** ou **AbrirFunção** se estiver usando o ambiente de the projeto do Access (.adp).

## <a name="setting"></a>Configuração

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
<td><p>O nome da consulta a ser aberta. A caixa de <strong>Nome de consulta</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todas as consultas no banco de dados atual. Esse é um argumento necessário. Se você executar uma macro que contém a ação <strong>AbrirConsulta</strong> em um banco de dados biblioteca, o Microsoft Access procurará primeiro a consulta com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</p></td>
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


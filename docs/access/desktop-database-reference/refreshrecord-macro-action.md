---
title: Ação da macro AtualizarRegistro
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d8682c19686650ab193536658c6b56961f289174
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307069"
---
# <a name="refreshrecord-macro-action"></a>Ação da macro AtualizarRegistro


**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos registros no conjunto atual.

## <a name="remarks"></a>Comentários

A ação **AtualizarRegistro** mostra somente as alterações feitas em registros no conjunto atual. Como a ação **AtualizarRegistro** não repete consultas ao banco de dados, o conjunto atual não incluirá registros que foram adicionados nem excluirá registros que foram excluídos após a última repetição de consulta ao banco de dados. Além disso, não excluirá os registros que não mais satisfaçam os critérios da consulta ou do filtro. Para repetir a consulta ao banco de dados, utilize o método **[Repetir consulta](requery-macro-action.md)**. Quando a fonte do registro de um formulário for consultada novamente, o conjunto atual de registros refletirá corretamente todos os dados da fonte do registro. .

O comportamento desta ação de macro depende do fato de estar sendo chamada em um banco de dados cliente ou em um banco de dados da Web.

## <a name="client-database"></a>Banco de dados cliente

Em um banco de dados cliente, você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos dados no conjunto atual. É equivalente ao método **[Atualizar](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**.

A ação de macro **AtualizarRegistro** executa as seguintes ações em um banco de dados cliente:

1.  Atualiza a fonte do registro para o formulário ou para a folha de dados ativa para refletir as alterações feitas nas linhas do conjunto atual.

2.  Atualiza o conjunto atual para refletir as alterações. Se uma linha da fonte do registro tiver sido excluída, ela será alterada para \#mostrar excluído.

3.  Atualiza o Active ou a folha de dos para exibir quaisquer registros alterados e registros \#excluídos, no conjunto atual.

4.  Repete consultas em todos os subformulários e subrelatórios no formulário ou na folha de dados ativa.

## <a name="web-database"></a>Banco de dados da Web

Em um banco de dados da Web, você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos registros no conjunto atual. As alterações incluem aquelas feitas pelo usuário atual ou por outros usuários.

A ação de macro **AtualizarRegistro** executa as seguintes ações em um banco de dados da Web:

1.  Recupera alterações do servidor para quaisquer tabelas de base no conjunto atual. Para tabelas ODBC vinculadas, recuperada alterações nos registros no conjunto atual da fonte de dados.

2.  Atualiza o conjunto atual para refletir as alterações. Se uma linha no conjunto atual tiver sido excluída, ela será alterada para mostrar \#excluído.

3.  Atualiza o formulário ou folha de de dos ativos para exibir quaisquer registros alterados e registros \#excluídos, no conjunto atual.

4.  Repete consultas em todos os subformulários e subrelatórios no formulário ou na folha de dados ativa.


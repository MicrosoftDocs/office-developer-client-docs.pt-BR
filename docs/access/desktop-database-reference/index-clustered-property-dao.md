---
title: Propriedade index. Clustered (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291849"
---
# <a name="indexclustered-property-dao"></a>Propriedade index. Clustered (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que indica se um objeto **Index** representa um índice agrupado para uma tabela (apenas espaços de trabalho do Microsoft Access). **Boolean** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Agrupado

*expressão* Uma expressão que retorna um objeto **index** .

## <a name="remarks"></a>Comentários

O valor definido ou retornado é um tipo de dados Booliano que será **True** se o objeto **Index** representar um índice agrupado.

Alguns formatos de banco de dados de desktop IISAM usam índices agrupados que consistem em um ou mais campos não-chave que juntos organizam todos os registros de uma tabela em uma ordem predefinida. Um índice agrupado fornece acesso eficiente aos registros em uma tabela nos quais os valores de índice podem não ser exclusivos.

A propriedade **Clustered** é de leitura/gravação para um novo objeto **Index** ainda não acrescentado a uma coleção e somente leitura para um objeto **Index** existente em uma coleção **Indexes**.

> [!NOTE]
> - Os bancos de dados do mecanismo de banco de dados do Microsoft Access ignoram a propriedade **Clustered** porque esse mecanismo não fornece suporte a índices agrupados.
> - Para fontes de dados ODBC, **** a propriedade Clustered sempre retorna **false**; Ele não detecta se a fonte de dados ODBC tem um índice agrupado ou não.



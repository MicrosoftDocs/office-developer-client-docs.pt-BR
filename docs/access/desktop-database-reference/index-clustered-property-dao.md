---
title: Propriedade Index.Clustered (DAO)
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
ms.openlocfilehash: 95b12df62fe47779c1867a291018726ada299390
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998928"
---
# <a name="indexclustered-property-dao"></a>Propriedade Index.Clustered (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica se um objeto **Index** representa um índice agrupado para uma tabela (apenas espaços de trabalho do Microsoft Access). **Boolean** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Em cluster

*expressão* Uma expressão que retorna um objeto **Index** .

## <a name="remarks"></a>Comentários

O valor definido ou retornado é um tipo de dados Booliano que será **True** se o objeto **Index** representar um índice agrupado.

Alguns formatos de banco de dados de desktop IISAM usam índices agrupados que consistem em um ou mais campos não-chave que juntos organizam todos os registros de uma tabela em uma ordem predefinida. Um índice agrupado fornece acesso eficiente aos registros em uma tabela nos quais os valores de índice podem não ser exclusivos.

A propriedade **Clustered** é de leitura/gravação para um novo objeto **Index** ainda não acrescentado a uma coleção e somente leitura para um objeto **Index** existente em uma coleção **Indexes**.

> [!NOTE]
> - Os bancos de dados do mecanismo de banco de dados do Microsoft Access ignoram a propriedade **Clustered** porque esse mecanismo não fornece suporte a índices agrupados.
> - Para fontes de dados ODBC, a propriedade **Clustered** sempre retorna **False**; ele não detecta se a fonte de dados ODBC tem um índice agrupado ou não.



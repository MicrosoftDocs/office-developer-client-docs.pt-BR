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
ms.openlocfilehash: 4e7bd39d3329c83ec2a26fbef11e3a3b4e51e760
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921297"
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
> <UL>
> <LI>
> <P>Os bancos de dados do mecanismo de banco de dados do Microsoft Access ignoram a propriedade <STRONG>Clustered</STRONG> porque esse mecanismo não fornece suporte a índices agrupados.</P>
> <LI>
> <P>Para fontes de dados ODBC, a propriedade <STRONG>Clustered</STRONG> sempre retorna <STRONG>False</STRONG>; ele não detecta se a fonte de dados ODBC tem um índice agrupado ou não.</P></LI></UL>



---
title: Método QueryDef.Close (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719999"
---
# <a name="querydefclose-method-dao"></a>Método QueryDef.Close (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Fecha um objeto **QueryDef** aberto.

## <a name="syntax"></a>Sintaxe

*expressão* . Fechar

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

Se o objeto **QueryDef** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.

Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).


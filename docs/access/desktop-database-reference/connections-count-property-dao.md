---
title: Propriedade Connections.Count (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec8ff4d610ef9a9b88f379ff8cc72d1b647f9bb2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871903"
---
# <a name="connectionscount-property-dao"></a>Propriedade Connections.Count (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna o número de objetos **[Connection](connection-object-dao.md)** na coleção **[Connections](connections-collection-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . Contagem

*expressão* Uma variável que representa um objeto **Connections** .

## <a name="remarks"></a>Comentários

Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.

A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.


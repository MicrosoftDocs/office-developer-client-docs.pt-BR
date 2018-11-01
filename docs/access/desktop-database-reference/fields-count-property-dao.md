---
title: Propriedade Fields.Count (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f788b726f5be7cdfd7531d4522b6c653744d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886743"
---
# <a name="fieldscount-property-dao"></a>Propriedade Fields.Count (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna o número de objetos da coleção especificada. **Integer** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Contagem

*expressão* Uma variável que representa um objeto **Fields** .

## <a name="remarks"></a>Comentários

Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.

A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.


---
title: Propriedade Relations.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1be0766c1f1a2057e5cb7137d2e9131a2505f75
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876005"
---
# <a name="relationscount-property-dao"></a>Propriedade Relations.Count (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna o número de objetos na coleção especificada. Somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Contagem

*expressão* Uma variável que representa um objeto **Relations** .

## <a name="remarks"></a>Comentários

Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.

A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.


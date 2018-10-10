---
title: Propriedade Errors (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b554b88153e79dfc1909bd55d95a3c3e48a855e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465040"
---
# <a name="errorscount-property-dao"></a>Propriedade Errors (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna o número de objetos na coleção especificada. Somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Contagem

*expressão* Uma variável que representa um objeto **Errors** .

## <a name="remarks"></a>Comentários

Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.

A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.


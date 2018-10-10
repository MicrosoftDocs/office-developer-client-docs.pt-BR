---
title: Propriedade QueryDefs.Count (DAO)
TOCTitle: Count Property
ms:assetid: 8caa01c5-692f-95e4-4b11-6e6c591f5872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197340(v=office.15)
ms:contentKeyID: 48546240
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be630e54ef55fae335347dabd61440dfe457c5ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463962"
---
# <a name="querydefscount-property-dao"></a>Propriedade QueryDefs.Count (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna o número de objetos na coleção especificada. Somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Contagem

*expressão* Uma variável que representa um objeto **QueryDefs** .

## <a name="remarks"></a>Comentários

Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.

A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.


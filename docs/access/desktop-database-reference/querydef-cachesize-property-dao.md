---
title: Propriedade QueryDef. caChesize (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301089"
---
# <a name="querydefcachesize-property-dao"></a>Propriedade QueryDef. caChesize (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna vários registros recuperados de uma fonte de dados ODBC que serão armazenados em cache localmente. **Long** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Ches

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

O valor da propriedade **CacheSize** deve estar entre 5 e 1200, mas não pode ser maior do que a memória disponível permitir. Um valor comum é 100. Uma definição de 0 desativa o armazenamento em cache.

O mecanismo de banco de dados do Microsoft Access solicita os registros dentro do intervalo de cache, a partir do cache, e solicita os registros fora do intervalo de cache a partir do servidor.

Os registros recuperados do cache não refletem as alterações simultâneas que outros usuários fizeram na fonte de dados.


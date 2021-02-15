---
title: Método Append (Índices do ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297092"
---
# <a name="append-method-adox-indexes"></a>Método Append (Índices do ADOX)


**Aplica-se ao:** Access 2013, Office 2013



Adiciona um novo objeto [Index](index-object-adox.md) à coleção [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Índices*. Append *Index* \[ ,*Columns*\]

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Índice* |O objeto **Index** a ser anexado ou o nome do índice a ser criado e anexado.|
|*Columns* |Opcional. Um valor **Variant** que especifica um ou mais nomes de colunas a serem indexadas. O parâmetro *Columns* corresponde ao(s) valor(es) da propriedade [Name](name-property-adox.md) de um ou mais objetos [Column](column-object-adox.md).|

## <a name="remarks"></a>Comentários

O parâmetro *Columns* pode receber o nome de uma coluna ou uma matriz de nomes de colunas.

Ocorrerá um erro se o provedor não oferecer suporte para a criação de índices.


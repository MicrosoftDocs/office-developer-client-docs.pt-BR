---
title: Método Append (Índices do ADOX)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f91535075c2782861dc409a6c527f159cd5458a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462776"
---
# <a name="append-method-adox-indexes"></a>Método Append (Índices do ADOX)


**Aplica-se a**: Access 2013 | Office 2013



Adiciona um novo objeto [Index](index-object-adox.md) à coleção [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Índices*. Acrescentar*índice* \[,*colunas*\]

## <a name="parameters"></a>Parâmetros

  - *Index*

  - O objeto **Index** a ser anexado ou o nome do índice a ser criado e anexado.

  - *Columns*

  - Opcional. Um valor **Variant** que especifica um ou mais nomes de colunas a serem indexadas. O parâmetro *Columns* corresponde aos valores da propriedade [Name](name-property-adox.md) de um objeto [Column](column-object-adox.md) ou objetos.

## <a name="remarks"></a>Comentários

O parâmetro *Columns* pode levar o nome de uma coluna ou uma matriz de nomes de coluna.

Ocorrerá um erro se o provedor não oferecer suporte para a criação de índices.


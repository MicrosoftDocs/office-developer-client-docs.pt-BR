---
title: Método Append (Tabelas do ADOX)
TOCTitle: Append method (ADOX Tables)
ms:assetid: 9e9fd57c-a856-6179-013f-9f378c3b7df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249726(v=office.15)
ms:contentKeyID: 48546664
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2bf2479c2a34291f245783ebaecd75ba31d2ac8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297071"
---
# <a name="append-method-adox-tables"></a>Método Append (Tabelas do ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Adiciona um novo objeto [Table](table-object-adox.md) à coleção [Tables](tables-collection-adox.md).

## <a name="syntax"></a>Sintaxe

*Tabelas*. Append *Table*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Table* | Um valor **Variant** que contém uma referência à **Tabela** a ser anexada ou ao nome da tabela a ser criada e anexada.|

## <a name="remarks"></a>Comentários

Ocorrerá um erro se o provedor não oferecer suporte à criação de tabelas.


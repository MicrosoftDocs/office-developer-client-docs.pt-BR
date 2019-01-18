---
title: Propriedades dinâmicas do conjunto de registros em XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712831"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Propriedades dinâmicas do conjunto de registros em XML

**Aplica-se a**: Access 2013, o Office 2013

As propriedades específicas do provedor do **Recordset** a seguir (do Mecanismo de cursor do cliente) são mantidas atualmente no formato XML:

- **AutoRecalc**
- **BatchSize**
- **CommandTimeout**
- **IRowsetChange**
- **IRowsetUpdate**
- **Reshape Name**
- **Resync Command**
- **Unique Catalog**
- **Unique Schema**
- **Unique Table**
- **Update Resync**
- **UpdateCriteria**


Essas propriedades são salvas na seção de esquema como atributos da definição do elemento do **Recordset** que está sendo mantido. Esses atributos são definidos no namespace do esquema do conjunto de linhas e deve ter o prefixo "rs:".

## <a name="see-also"></a>Confira também

- [Propriedades dinâmicas do ADO](ado-dynamic-properties.md)

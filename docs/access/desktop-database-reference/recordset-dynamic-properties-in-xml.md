---
title: Propriedades dinâmicas do recordset em XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4193220e450c59e7293ed6befa37d8da23801f27
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462299"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Propriedades dinâmicas do recordset em XML


**Aplica-se a**: Access 2013 | Office 2013

## <a name="recordset-dynamic-properties-in-xml"></a>Propriedades dinâmicas do recordset em XML

As propriedades específicas do provedor do **Recordset** a seguir (do Mecanismo de cursor do cliente) são mantidas atualmente no formato XML:

  - **Update Resync**

  - **Unique Table**

  - **Unique Schema**

  - **Unique Catalog**

  - **Resync Command**

  - **IRowsetChange**

  - **IRowsetUpdate**

  - **CommandTimeout**

  - **BatchSize**

  - **UpdateCriteria**

  - **Reshape Name**

  - **AutoRecalc**

Essas propriedades são salvas na seção de esquema como atributos da definição do elemento do **Recordset** que está sendo mantido. Esses atributos são definidos no namespace do esquema do conjunto de linhas e deve ter o prefixo "rs:".


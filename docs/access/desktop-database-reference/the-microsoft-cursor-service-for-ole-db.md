---
title: Microsoft Cursor Service for OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722617"
---
# <a name="microsoft-cursor-service-for-ole-db"></a>Serviço de cursor da Microsoft para OLE DB


**Aplica-se a**: Access 2013, o Office 2013

Ao selecionar um cursor do cliente ou definir a propriedade **CursorLocation** como **adUseClient**, você está chamando o Microsoft Cursor Service for OLE DB. Também é possível ver referências ao "Mecanismo de cursor do cliente", que é essencialmente a mesma coisa no contexto do ADO. Esse serviço suplementa as funções de suporte ao cursor dos provedores de dados. Como resultado, pode-se observar uma funcionalidade relativamente uniforme de todos os provedores de dados.

O Serviço de cursor para OLE DB disponibiliza as propriedades dinâmicas e aprimora o comportamento de certos métodos. Por exemplo, a propriedade dinâmica **Optimize** permite a criação de índices temporários para facilitar determinadas operações, como o método **Find**.

O Serviço de cursor habilita o suporte para atualização em lotes em todos os casos. Além disso, ele simula tipos de cursores com mais recursos, como os cursores dinâmicos, quando um provedor de dados só pode fornecer cursores com menos recursos como os estáticos.


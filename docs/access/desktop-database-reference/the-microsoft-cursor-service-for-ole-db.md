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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314354"
---
# <a name="microsoft-cursor-service-for-ole-db"></a>Serviço de cursor da Microsoft para OLE DB


**Aplica-se ao:** Access 2013, Office 2013

Ao selecionar um cursor do cliente ou definir a propriedade **CursorLocation** como **adUseClient**, você está chamando o Microsoft Cursor Service for OLE DB. Também é possível ver referências ao "Mecanismo de cursor do cliente", que é essencialmente a mesma coisa no contexto do ADO. Esse serviço suplementa as funções de suporte ao cursor dos provedores de dados. Como resultado, pode-se observar uma funcionalidade relativamente uniforme de todos os provedores de dados.

O Serviço de cursor para OLE DB disponibiliza as propriedades dinâmicas e aprimora o comportamento de certos métodos. Por exemplo, a propriedade dinâmica **Optimize** permite a criação de índices temporários para facilitar determinadas operações, como o método **Find**.

O Serviço de cursor habilita o suporte para atualização em lotes em todos os casos. Além disso, ele simula tipos de cursores com mais recursos, como os cursores dinâmicos, quando um provedor de dados só pode fornecer cursores com menos recursos como os estáticos.


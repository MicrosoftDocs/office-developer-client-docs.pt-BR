---
title: Microsoft Cursor Service for OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b84899cc4dd8a85cc48ab26057935c9ab150361
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464657"
---
# <a name="the-microsoft-cursor-service-for-ole-db"></a>Microsoft Cursor Service for OLE DB


**Aplica-se a**: Access 2013 | Office 2013

Ao selecionar um cursor do cliente ou definir a propriedade **CursorLocation** como **adUseClient**, você está chamando o Microsoft Cursor Service for OLE DB. Também é possível ver referências ao "Mecanismo de cursor do cliente", que é essencialmente a mesma coisa no contexto do ADO. Esse serviço suplementa as funções de suporte ao cursor dos provedores de dados. Como resultado, pode-se observar uma funcionalidade relativamente uniforme de todos os provedores de dados.

O Serviço de cursor para OLE DB disponibiliza as propriedades dinâmicas e aprimora o comportamento de certos métodos. Por exemplo, a propriedade dinâmica **Optimize** permite a criação de índices temporários para facilitar determinadas operações, como o método **Find**.

O Serviço de cursor habilita o suporte para atualização em lotes em todos os casos. Além disso, ele simula tipos de cursores com mais recursos, como os cursores dinâmicos, quando um provedor de dados só pode fornecer cursores com menos recursos como os estáticos.


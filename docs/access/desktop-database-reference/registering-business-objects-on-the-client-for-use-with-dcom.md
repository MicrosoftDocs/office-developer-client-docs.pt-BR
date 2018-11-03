---
title: Registrar objetos de negócios no cliente para usam com o DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2746ad6d0736f4415788cde477e1513d9b46146
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946801"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Registrar objetos de negócios no cliente para usam com o DCOM

**Aplica-se a**: Access 2013, o Office 2013

Os objetos de negócios personalizados precisam garantir que o lado clientepode mapear seu nome de programa (ProgId) para um identificador (CLSID) que pode ser usado por DCOM. Por esse motivo, o ProgID do objeto DCOM deve estar no registro do lado cliente e mapeado para o ID de classe do objeto de negócios do lado servidor. Para os outros protocolos com suporte (HTTP, HTTPS e em andamento), isso não é necessário.

Por exemplo, se você expuser um objeto de negócios do lado servidor chamado MyBObj com um ID de classe específico, por exemplo, "{00112233-4455-6677-8899-00AABBCCDDEE}", certifique-se de que as seguintes entradas serão adicionadas ao registro do lado cliente:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```


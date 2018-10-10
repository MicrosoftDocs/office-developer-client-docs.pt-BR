---
title: Registrando objetos de negócios no cliente para uso com o DCOM
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f3d29d20200b6e435ffafaaa35c7f507b88b939
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463589"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Registrando objetos de negócios no cliente para uso com o DCOM


**Aplica-se a**: Access 2013 | Office 2013

Os objetos de negócios personalizados precisam garantir que o lado clientepode mapear seu nome de programa (ProgId) para um identificador (CLSID) que pode ser usado por DCOM. Por esse motivo, o ProgID do objeto DCOM deve estar no registro do lado cliente e mapeado para o ID de classe do objeto de negócios do lado servidor. Para os outros protocolos com suporte (HTTP, HTTPS e em andamento), isso não é necessário.

Por exemplo, se você expuser um objeto de negócios do lado servidor chamado MyBObj com um ID de classe específico, por exemplo, "{00112233-4455-6677-8899-00AABBCCDDEE}", certifique-se de que as seguintes entradas serão adicionadas ao registro do lado cliente:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```


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
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="0dc56-102">Registrar objetos de negócios no cliente para usam com o DCOM</span><span class="sxs-lookup"><span data-stu-id="0dc56-102">Registering business objects on the client for use with DCOM</span></span>

<span data-ttu-id="0dc56-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dc56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0dc56-p101">Os objetos de negócios personalizados precisam garantir que o lado clientepode mapear seu nome de programa (ProgId) para um identificador (CLSID) que pode ser usado por DCOM. Por esse motivo, o ProgID do objeto DCOM deve estar no registro do lado cliente e mapeado para o ID de classe do objeto de negócios do lado servidor. Para os outros protocolos com suporte (HTTP, HTTPS e em andamento), isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="0dc56-p101">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM. For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object. For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="0dc56-107">Por exemplo, se você expuser um objeto de negócios do lado servidor chamado MyBObj com um ID de classe específico, por exemplo, "{00112233-4455-6677-8899-00AABBCCDDEE}", certifique-se de que as seguintes entradas serão adicionadas ao registro do lado cliente:</span><span class="sxs-lookup"><span data-stu-id="0dc56-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```


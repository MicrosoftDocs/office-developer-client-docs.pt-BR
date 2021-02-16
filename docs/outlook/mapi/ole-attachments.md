---
title: Anexos OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb716ce014ec3c4b21ce2b021c1a9f6f291d511c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417144"
---
# <a name="ole-attachments"></a>Anexos OLE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Anexos que são objetos OLE são codificados como objetos de fluxo OLE 1 para compatibilidade com compatibilidade com backward. Se o objeto original for realmente um objeto OLE 2 **IStorage,** o objeto deverá ser convertido em um fluxo OLE 1. Essa conversão é realizada usando a **função OleConvertIStorageToOLESTREAM,** que faz parte das bibliotecas OLE do Win32. 
  


---
title: Anexos OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ccd4a77e74a4a4cbdfcd8474d4cc00d0d0516839
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584636"
---
# <a name="ole-attachments"></a>Anexos OLE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Anexos que sejam objetos OLE são codificados como objetos stream de OLE 1 para compatibilidade com versões anteriores. Se o objeto original é realmente um objeto OLE 2 **IStorage** , o objeto deve ser convertido para um fluxo de OLE 1. Essa conversão é realizada usando a função **OleConvertIStorageToOLESTREAM** , que é parte das bibliotecas Win32 OLE. 
  


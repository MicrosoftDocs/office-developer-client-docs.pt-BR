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
ms.openlocfilehash: b95b83ad7eedff577e4c36365c9e451f4b458173
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768160"
---
# <a name="ole-attachments"></a>Anexos OLE

  
  
**Aplica-se a**: Outlook 
  
Anexos que sejam objetos OLE são codificados como objetos stream de OLE 1 para compatibilidade com versões anteriores. Se o objeto original é realmente um objeto OLE 2 **IStorage** , o objeto deve ser convertido para um fluxo de OLE 1. Essa conversão é realizada usando a função **OleConvertIStorageToOLESTREAM** , que é parte das bibliotecas Win32 OLE. 
  


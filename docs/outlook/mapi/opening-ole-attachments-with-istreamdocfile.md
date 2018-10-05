---
title: Abertura de anexos OLE com IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Modificado pela última vez: 06 de julho de 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386548"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Abertura de anexos OLE com IStreamDocfile

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao abrir um anexo do objeto OLE, use a interface de **IStreamDocfile** ao invés [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fornece acesso direto ao objeto usando armazenamento estruturado, eliminando a necessidade de realizar uma operação de cópia e reduz a sobrecarga. **IStreamDocfile** é uma implementação específica da **IStream** com o conteúdo do stream garantido a ser formatado como armazenamento estruturado. **IStreamDocfile** é implementado por provedores de armazenamento de mensagem. 
  


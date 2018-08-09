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
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768194"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Abertura de anexos OLE com IStreamDocfile

**Aplica-se a**: Outlook 
  
Ao abrir um anexo do objeto OLE, use a interface de **IStreamDocfile** ao invés [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** fornece acesso direto ao objeto usando armazenamento estruturado, eliminando a necessidade de realizar uma operação de cópia e reduz a sobrecarga. **IStreamDocfile** é uma implementação específica da **IStream** com o conteúdo do stream garantido a ser formatado como armazenamento estruturado. **IStreamDocfile** é implementado por provedores de armazenamento de mensagem. 
  


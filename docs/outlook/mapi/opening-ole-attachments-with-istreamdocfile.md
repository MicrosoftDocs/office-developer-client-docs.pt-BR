---
title: Abrir anexos OLE com IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326226"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Abrir anexos OLE com IStreamDocfile

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao abrir um anexo de objeto OLE, use a interface **IStreamDocfile** em vez de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**O IStreamDocfile** fornece acesso direto ao objeto usando armazenamento estruturado, eliminando a necessidade de executar uma operação de cópia e reduzindo a sobrecarga. **IStreamDocfile** é uma implementação específica do **IStream com** o conteúdo do fluxo garantido para ser formatado como armazenamento estruturado. **O IStreamDocfile** é implementado pelos provedores de armazenamento de mensagens. 
  


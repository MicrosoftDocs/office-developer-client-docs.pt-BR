---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c1a78889ea98133af46089fdc93b0c1c4bb24226
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768038"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Aplica-se a**: Outlook 
  
Diminui a contagem de referência, limpa e exclui por instância dados globais para a DLL de MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum 
  
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Um aplicativo cliente chama a função **MAPIUninitialize** para encerrar sua interação com MAPI, começado com uma chamada para a função [MAPIInitialize](mapiinitialize.md) . Após a chamada **MAPIUninitialize** , nenhuma outra chamada MAPI pode ser feita pelo cliente. 
  
 **MAPIUninitialize** diminui a contagem de referência e a função **MAPIInitialize** correspondente incrementa a contagem de referência. Assim, o número de chamadas para uma função deve ser igual o número de chamadas para outro. 
  
> [!NOTE]
> Você não pode chamar **MAPIInitialize** ou **MAPIUninitialize** de dentro de uma função do Win32 **DllMain** ou qualquer outra função que cria ou finaliza threads. Para obter mais informações, consulte [Usando objetos de Thread-Safe](using-thread-safe-objects.md). 
  


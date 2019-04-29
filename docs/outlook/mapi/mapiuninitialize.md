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
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408520"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Decrementa a contagem de referência, limpa e exclui dados globais por instância da DLL MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum 
  
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Um aplicativo cliente chama a função **MAPIUninitialize** para finalizar sua interação com MAPI, iniciado com uma chamada para a função [MAPIInitialize](mapiinitialize.md) . Após a chamada de **MAPIUninitialize** , nenhuma outra chamada MAPI pode ser feita pelo cliente. 
  
 **MAPIUninitialize** decrementa a contagem de referência, e a função **MAPIInitialize** correspondente incrementa a contagem de referência. Portanto, o número de chamadas para uma função deve ser igual ao número de chamadas para o outro. 
  
> [!NOTE]
> Você não pode chamar o **MAPIInitialize** ou o **MAPIUninitialize** de dentro de uma função **DllMain** do Win32 ou qualquer outra função que crie ou encerre threads. Para obter mais informações, consulte [usando objetos isentos de threads](using-thread-safe-objects.md). 
  


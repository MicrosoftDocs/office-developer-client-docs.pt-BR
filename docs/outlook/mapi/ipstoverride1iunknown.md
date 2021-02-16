---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315495"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que um provedor de armazenamento de pastas particulares (PST) substitua a política PSTDisableGrow.
  
|||
|:-----|:-----|
|Herda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> |Provedor de armazenamento PST  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Recupera a lista de registros do arquivo de Pastas Particulares (.pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registra arquivos de Pastas Particulares para desbloqueio automático, evitando chamadas para HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Desbloqueia um arquivo de Pastas Particulares para crescimento.  <br/> |
   
## <a name="remarks"></a>Comentários

Os Identificadores da Interface do Manipulador de Substituição de PST podem não estar definidos no arquivo de header baixável que você tem atualmente, nesse caso, você os encontrará no tópico Constantes de [MAPI](mapi-constants.md) e poderá copiá-los e adicioná-los ao seu código. Use a DEFINE_GUID macro definida no arquivo de título guiddef.h do Microsoft Software Development Kit do Windows (SDK) para associar nomes simbólicos de identificador global exclusivo (GUID) a seus valores. 
  
For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)


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
  
Permite que um provedor de repositório de arquivos de pastas particulares (PST) substitua a política PSTDisableGrow.
  
|||
|:-----|:-----|
|Herda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> |Provedor de repositório PST  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Recupera a lista de registros para o arquivo de pastas particulares (. pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registra arquivos de pastas pessoais para desbloqueio automático, evitando outras chamadas para o HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Desbloqueia um arquivo de pastas particulares para crescimento.  <br/> |
   
## <a name="remarks"></a>Comentários

Os identificadores de interface do manipulador de substituição de PST podem não ser definidos no arquivo de cabeçalho que pode ser baixado e, nesse caso, você irá encontrá-los no tópico de [constantes de MAPI](mapi-constants.md) e pode copiá-los e adicioná-los ao seu código. Use a macro DEFINE_GUID definida no arquivo de cabeçalho do Microsoft Windows Software Development Kit (SDK) guiddef. h para associar nomes simbólicos de identificador global exclusivo (GUID) a seus valores. 
  
Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)


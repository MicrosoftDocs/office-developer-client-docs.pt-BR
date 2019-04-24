---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356977"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Acessa recursos de um provedor de repositório de arquivos de pastas particulares (PST).
  
|||
|:-----|:-----|
|Herda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> |Provedor de repositório PST  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Inicia o procedimento de desbloqueio para um arquivo de pastas particulares (. pst).  <br/> |
   
## <a name="remarks"></a>Comentários

Os identificadores de interface do manipulador de substituição de PST podem não ser definidos no arquivo de cabeçalho que pode ser baixado e, nesse caso, você irá encontrá-los no tópico de [constantes de MAPI](mapi-constants.md) e pode copiá-los e adicioná-los ao seu código. Use a macro DEFINE_GUID definida no arquivo de cabeçalho do Microsoft Windows Software Development Kit (SDK) guiddef. h para associar nomes simbólicos de identificador global exclusivo (GUID) a seus valores. 
  
Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)


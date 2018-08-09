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
ms.openlocfilehash: 6ee4524d08e334df858c2f035f1b21bd2b0a1c8b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767675"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Provedor de armazenamento de recursos de acessos de um arquivo de pastas particulares (. PST).
  
|||
|:-----|:-----|
|Herda de:  <br/> |IUnknown  <br/> |
|Implementada por:  <br/> |Provedor de repositórios de PST  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Inicia o procedimento desbloqueando um arquivo de pastas particulares (. pst).  <br/> |
   
## <a name="remarks"></a>Comentários

Os identificadores de Interface de manipulador substituir PST não poderão ser definidos no arquivo de cabeçalho para download que você possui atualmente, caso em que você irá encontrá-las no tópico [Constantes MAPI](mapi-constants.md) e pode copiar e adicioná-los ao seu código. Use a macro DEFINE_GUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar nomes simbólicos de identificador globalmente exclusivo (GUID) com seus valores. 
  
Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)


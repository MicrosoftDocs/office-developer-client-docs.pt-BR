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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: db2853080b1fc2ff3a346dcfb8d112237b7f3459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767682"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1: IUnknown

  
  
**Aplica-se a**: Outlook 
  
Permite que um provedor de armazenamento de arquivo (. PST) de pastas particulares substituir a política de PSTDisableGrow.
  
|||
|:-----|:-----|
|Herda de:  <br/> |IUnknown  <br/> |
|Implementada por:  <br/> |Provedor de repositórios de PST  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Recupera a lista dos registros para o arquivo de pastas particulares (. pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registra os arquivos de pastas particulares para desbloqueio automático, evitando mais chamadas para HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Desbloqueia um arquivo de pastas particulares para crescimento.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Os identificadores de Interface de manipulador substituir PST não poderão ser definidos no arquivo de cabeçalho para download que você possui atualmente, caso em que você irá encontrá-las no tópico [Constantes MAPI](mapi-constants.md) e pode copiar e adicioná-los ao seu código. Use a macro DEFINE_GUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar nomes simbólicos de identificador globalmente exclusivo (GUID) com seus valores. 
  
Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Confira também



[IPSTOVERRIDEREQ: IUnknown](ipstoverridereqiunknown.md)


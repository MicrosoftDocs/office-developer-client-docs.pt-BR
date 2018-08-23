---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cb4f38615ac6cacb3acbaa456f0992bf55c3653d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568620"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Garante que o método **OpenEntry** for aberto, o provedor de catálogo de endereços do Exchange esperado. Essa função funciona da mesma forma para [IAddrBook::Details](iaddrbook-details.md) , mas abre **entryID** usando o catálogo de endereços do Exchange identificado pela _pEmsabpUID_.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _pEmsabpUID_
  
> [in] Um ponteiro para uma _emsabpUID_ que identifica o provedor de catálogo de endereços do Exchange essa função deve usar para exibir detalhes sobre o identificador de entrada. Se o identificador de entrada de entrada não é um identificador de entrada do Exchange endereço livro provedor, esse parâmetro será ignorado e a age de chamada de função exatamente como [IAddrBook::Details](iaddrbook-details.md). Se esse parâmetro for NULL ou um zero MAPIUID, essa função também funciona exatamente como [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser NULL.
    
 _lpulUIParam_
  
> [out] Uma alça para a janela pai para a caixa de diálogo.
    
 _lpfnDismiss_
  
> [in] Um ponteiro para uma função com base no **DISMISSMODELESS** protótipo ou nulo. Este membro só se aplica a versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário descarte a caixa de diálogo sem janela restrita endereço informando um cliente que está chamando que a caixa de diálogo não está mais ativa de detalhes. 
    
 _lpvDismissContext_
  
> [in] Um ponteiro para informações de contexto para passar para a função **DISMISSMODELESS** apontado pelo parâmetro _lpfnDismiss_ . Esse parâmetro se aplica somente à versão da caixa de diálogo sem janela restrita, incluindo o sinalizador **DIALOG_SDI** no parâmetro _ulFlags_ . 
    
 _cbEntryID_
  
> [in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.
    
 _lpfButtonCallback_
  
> [in] Um ponteiro para uma função com base no protótipo de função **LPFNBUTTON** . Uma função **LPFNBUTTON** adiciona um botão para a caixa de diálogo detalhes. 
    
 _lpvButtonContext_
  
> [in] Um ponteiro para os dados que foi usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível. O parâmetro _lpszButtonText_ deve ser NULL quando um botão extensível não é necessário. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo do texto para o parâmetro _lpszButtonText_ . Sinalizadores a seguir podem ser definidos: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que detalhes retorna TRUE se as alterações são feitas na verdade, o endereço; Caso contrário, detalhes retorna FALSE.
    
DIALOG_MODAL
  
> Exibe a versão modal da caixa de diálogo endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
> Exibe a versão sem janela restrita da caixa de diálogo endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.
    
MAPI_UNICODE
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    


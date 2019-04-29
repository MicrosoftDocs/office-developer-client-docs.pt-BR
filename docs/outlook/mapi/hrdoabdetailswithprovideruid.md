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
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426678"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Garante que o método **OpenEntry** seja aberto pelo provedor de catálogo de endereços do Exchange esperado. Essa função funciona de forma semelhante a [IAddrBook::D etails](iaddrbook-details.md) , mas abre **EntryID** usando o catálogo de endereços do Exchange identificado por _pEmsabpUID_.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
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
  
> no Um ponteiro para um _emsabpUID_ que identifica o provedor do catálogo de endereços do Exchange essa função deve usar para exibir detalhes no identificador de entrada. Se o identificador de entrada de entrada não for um identificador de entrada do provedor de catálogo de endereços do Exchange, esse parâmetro será ignorado e a chamada de função atuará exatamente como [IAddrBook::D etails](iaddrbook-details.md). Se esse parâmetro for nulo ou um MAPIUID zero, essa função também funcionará exatamente como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> no O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser nulo.
    
 _lpulUIParam_
  
> bota Uma alça para a janela pai da caixa de diálogo.
    
 _lpfnDismiss_
  
> no Um ponteiro para uma função com base no protótipo **DISMISSMODELESS** ou nulo. Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido. MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente que está chamando os detalhes de que a caixa de diálogo não está mais ativa. 
    
 _lpvDismissContext_
  
> no Um ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** apontada pelo parâmetro _lpfnDismiss_ . Esse parâmetro se aplica apenas à versão sem janela restrita da caixa de diálogo, incluindo o sinalizador **DIALOG_SDI** no parâmetro _parâmetroulflags_ . 
    
 _cbEntryID_
  
> no A contagem de bytes do identificador de entrada especificado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.
    
 _lpfButtonCallback_
  
> no Um ponteiro para uma função com base no protótipo de função **LPFNBUTTON** . Uma função **LPFNBUTTON** adiciona um botão à caixa de diálogo detalhes. 
    
 _lpvButtonContext_
  
> no Um ponteiro para dados que foram usados como um parâmetro para a função especificada pelo parâmetro _lpfButtonCallback_ . 
    
 _lpszButtonText_
  
> no Um ponteiro para uma cadeia de caracteres que contém o texto a ser aplicado ao botão adicionado, se esse botão é extensível. O parâmetro _lpszButtonText_ deve ser NULL quando um botão extensível não é necessário. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de texto para o parâmetro _lpszButtonText_ . Os seguintes sinalizadores podem ser definidos: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que os detalhes retorna TRUE se as alterações forem realmente feitas no endereço; caso contrário, Details retornará FALSE.
    
DIALOG_MODAL
  
> Exibe a versão modal da caixa de diálogo endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
> Exibe a versão sem janela restrita da caixa de diálogo de endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.
    
MAPI_UNICODE
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    


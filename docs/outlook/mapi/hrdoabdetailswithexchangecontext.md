---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421365"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Garante que o método **OpenEntry** seja aberto pelo provedor de agenda do Exchange esperado. Essa função funciona de forma semelhante a [IAddrBook::D etails](iaddrbook-details.md), mas abre a **entryID** usando o livro de endereços do Exchange identificado pelo parâmetro _pEmsmdbUID._ 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a>Parâmetros

 _pmsess_
  
> O **IMAPISession conectado.** Não pode ser NULL.
    
 _pEmsmdbUID_
  
> Um ponteiro para **um emsmdbUID** que identifica o Serviço do Exchange que contém o provedor de agenda do Exchange que é usado pela função para abrir o identificador de entrada. Se o identificador de entrada de entrada não for um identificador de entrada do provedor de endereços do Exchange, esse parâmetro será ignorado e a função se comportará como [IAddrBook::OpenEntry](iaddrbook-openentry.md). Se esse parâmetro for NULL ou zero **MAPIUID,** essa função também atuará exatamente como [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] O livro de endereços usado para abrir o identificador de entrada. Não pode ser NULL.
    
 _lpulUIParam_
  
> [out] Um alça para a janela pai da caixa de diálogo.
    
 _lpfnDismiss_
  
> [in] Um ponteiro para uma função baseada no protótipo **DISMISSMODELESS** ou NULL. Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido. MAPI calls the **DISMISSMODELESS function** when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active. 
    
 _lpvDismissContext_
  
> [in] Um ponteiro para informações de contexto a ser passado para a **função DISMISSMODELESS** apontado pelo _parâmetro lpfnDismiss._ Esse parâmetro só se aplica à versão sem modo da caixa de diálogo incluindo o sinalizador **DIALOG_SDI** no _parâmetro ulFlags._ 
    
 _cbEntryID_
  
> [in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.
    
 _lpfButtonCallback_
  
> [in] Um ponteiro para uma função baseada no protótipo da função **LPFNBUTTON.** Uma **função LPFNBUTTON** adiciona um botão à caixa de diálogo de detalhes. 
    
 _lpvButtonContext_
  
> [in] Um ponteiro para dados que foi usado como um parâmetro para a função especificada pelo _parâmetro lpfButtonCallback._ 
    
 _lpszButtonText_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém texto a ser aplicado ao botão adicionado, se esse botão for extensível. O  _parâmetro lpszButtonText_ deve ser NULL quando não for necessário um botão extensível. 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o tipo de texto para o _parâmetro lpszButtonText._ Os sinalizadores a seguir podem ser definidos: 
    
AB_TELL_DETAILS_CHANGE
  
> Indica que Details retornará TRUE se as alterações realmente foram feitas no endereço; Caso contrário, Details retornará FALSE.
    
DIALOG_MODAL
  
> Exibe a versão modal da caixa de diálogo de endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_SDI.
    
DIALOG_SDI
  
> Exibe a versão sem modo da caixa de diálogo de endereço comum. Esse sinalizador é mutuamente exclusivo com DIALOG_MODAL.
    
MAPI_UNICODE
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    


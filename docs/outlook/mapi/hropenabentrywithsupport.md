---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417641"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Não use essa função.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parâmetros

 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta.
    
 _lpInterface_
  
>  [in] Um ponteiro para o IID (identificador de interface) da interface a ser usada para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão [é IMailUser : IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, é [IDistList : IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir  _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
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
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de entrada aberta.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro da entrada aberta.
    


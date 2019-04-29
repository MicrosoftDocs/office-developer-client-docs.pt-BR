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
|Arquivo de cabeçalho:  <br/> |abhelp. h  <br/> |
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
  
> no A contagem de bytes do identificador de entrada especificado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta.
    
 _lpInterface_
  
>  no Um ponteiro para o identificador de interface (IID) da interface a ser usado para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e, para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
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
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo de entrada aberta.
    
 _lppUnk_
  
> bota Um ponteiro para um ponteiro da entrada aberta.
    


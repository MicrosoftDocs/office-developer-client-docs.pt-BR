---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766821"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Aplica-se a**: Outlook 
  
Não use essa função.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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

## <a name="parameters"></a>Par�metros

 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir.
    
 _lpInterface_
  
>  [in] Um ponteiro para o identificador de interface (IID) da interface a ser usada para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, ele é [IDistList: IMAPIContainer](idistlistimapicontainer.md), e para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
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
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo da entrada aberta.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro da entrada aberta.
    


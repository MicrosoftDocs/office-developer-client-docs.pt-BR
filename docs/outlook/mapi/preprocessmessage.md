---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437242"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função que pré-processamento o conteúdo da mensagem ou o formato de uma mensagem.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
|Função definida implementada por:  <br/> |Provedores de transporte  <br/> |
|Função definida chamada por:  <br/> |Spooler MAPI  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a>Parâmetros

 _lpvSession_
  
> no Ponteiro para a sessão a ser usada. 
    
 _lpMessage_
  
> no Ponteiro para a mensagem a ser preprocessada. 
    
 _lpAdrBook_
  
> no Ponteiro para o catálogo de endereços do qual o usuário deve selecionar destinatários para a mensagem. 
    
 _lpFolder_
  
> [in, out] Ponteiro para uma pasta. Na entrada, o parâmetro _lpFolder_ aponta para a pasta que contém as mensagens a serem processadas. Na saída, _lpFolder_ aponta para a pasta onde as mensagens pré processadas foram colocadas. 
    
 _lpAllocateBuffer_
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado para alocar memória adicional onde for necessário. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória. 
    
 _lpcOutbound_
  
> bota Ponteiro para o número de mensagens na matriz apontadas pelo parâmetro _lpppMessage_ . 
    
 _lpppMessage_
  
> bota Ponteiro para um ponteiro para uma matriz de ponteiros para mensagens preprocessadas ou de outra forma geradas. 
    
 _lppRecipList_
  
> bota Ponteiro para uma estrutura [das ADRLIST](adrlist.md) retornada opcional, listando destinatários detectados pelo pré-processador para o qual a mensagem não é entregue. Para obter mais informações sobre o conteúdo dessa lista, consulte o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> O conteúdo da mensagem foi preprocessada com êxito.
    
## <a name="remarks"></a>Comentários

Um pré-processador de mensagem do provedor de transporte pode apresentar um indicador de progresso durante o pré-processamento da mensagem. No enTanto, ele nunca deve apresentar uma caixa de diálogo que exija interação do usuário durante o pré-processamento da mensagem. 
  
Quando um pré-processador adiciona grandes quantidades de dados a uma mensagem de saída, determinados procedimentos devem ser seguidos. Esse tipo de mensagem pode ser armazenado em um repositório de mensagens baseado em servidor, fazendo com que o pré-processador acesse um repositório remoto, um procedimento de consumo de tempo. Para evitar ter que fazer isso, o pré-processador deve ter uma opção que permite que ele armazene dados que contenham uma grande quantidade de espaço em um repositório de mensagens local e forneça uma referência a esse repositório local na mensagem. 
  
O pré-processador não deve liberar nenhum dos objetos passados originalmente para a função baseada em **PreprocessMessage** . 
  
Antes que o spooler MAPI possa chamar uma função **PreprocessMessage** , o provedor de transporte deve ter registrado a função em uma chamada para o método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) . Depois de chamar uma função **PreprocessMessage** , o spooler não pode continuar enviando uma mensagem até que a função retorne. 
  
O spooler MAPI é proprietário da tarefa de envio de mensagens. Isso significa que a mensagem original nunca é colocada em uma matriz de ponteiros de mensagem e que uma chamada para os métodos **SubmitMessage** nunca é necessária. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


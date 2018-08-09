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
ms.openlocfilehash: 22562e1177c9a649bc66b25b5e8e9e6ecc8e397c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770179"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Aplica-se a**: Outlook 
  
Define uma função que pré-processa o conteúdo da mensagem ou o formato de uma mensagem.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de transporte  <br/> |
|Função definido chamada pelo:  <br/> |Spooler MAPI  <br/> |
   
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
  
> [in] Ponteiro para a sessão a ser usado. 
    
 _lpMessage_
  
> [in] Ponteiro para a mensagem para ser processado. 
    
 _lpAdrBook_
  
> [in] Ponteiro para o catálogo de endereços do qual o usuário deve selecionar destinatários da mensagem. 
    
 _lpFolder_
  
> [além, out] Ponteiro para uma pasta. Na entrada, o parâmetro _lpFolder_ aponta para a pasta que contém mensagens para ser processado. Na saída, _lpFolder_ aponta para a pasta onde as mensagens pré-processado tiverem sido colocadas. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional onde necessário. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
 _lpcOutbound_
  
> [out] Ponteiro para o número de mensagens na matriz apontado pelo parâmetro _lpppMessage_ . 
    
 _lpppMessage_
  
> [out] Ponteiro para um ponteiro para uma matriz de ponteiros para preprocessada ou caso contrário gerada mensagens. 
    
 _lppRecipList_
  
> [out] Ponteiro para uma estrutura [ADRLIST](adrlist.md) retornado opcional, listando os destinatários pré-processador detectado para o qual a mensagem é entregue. Para obter mais informações sobre o conteúdo desta lista, consulte o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Conteúdo da mensagem foram pré-processados com êxito.
    
## <a name="remarks"></a>Comentários

Um pré-processador de mensagem do provedor de transporte pode representar um indicador de progresso durante a mensagem pré-processamento. No entanto, ele nunca deve apresentar uma caixa de diálogo exigir interação do usuário durante a mensagem pré-processamento. 
  
Quando um pré-processador adiciona grandes quantidades de dados a uma mensagem de saída, certos procedimentos devem ser seguidos. Esse tipo de mensagem pode ser armazenado em um armazenamento de mensagens baseado em servidor, causando o pré-processador acessar um repositório remoto, um procedimento demorado. Para evitar a fazer isso, o pré-processador deve ter uma opção que ativa para armazenar dados que utiliza uma grande quantidade de espaço em um repositório de mensagens local e para fornecer uma referência para esse repositório local na mensagem. 
  
O pré-processador não deve liberar qualquer um dos objetos originalmente passados para a função de **PreprocessMessage** com base. 
  
Antes do MAPI spooler pode chamar uma função de **PreprocessMessage** , o provedor de transporte deve ter registrado a função em uma chamada ao método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . Depois de chamar uma função **PreprocessMessage** , o spooler não pode continuar enviando uma mensagem até que a função retornará. 
  
O MAPI spooler possui a tarefa de envio de mensagens. Isso significa que a mensagem original nunca é colocada em uma matriz de ponteiros de mensagem e que uma chamada para os métodos **SubmitMessage** nunca é necessária. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


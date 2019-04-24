---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348612"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um novo objeto [IMessage](imessageimapiprop.md) na parte superior de um objeto OLE **IStorage** existente, para ser usado em uma sessão de mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>Parâmetros

_lpMsgSess_
  
> no Ponteiro para um objeto de sessão de mensagem dentro do qual o novo objeto **IMessage**-on- **IStorage** deve ser criado. 
    
_lpAllocateBuffer_
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória. 
    
_lpAllocateMore_
  
> no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado para alocar memória adicional. 
    
_lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória. 
    
_lpMalloc_
  
> no Ponteiro para um objeto de alocador de memória expondo a interface **IMalloc** do OLE. A interface **IMessage** precisa usar esse método de alocação ao trabalhar com interfaces como **IStorage** e **IStream**. 
    
_lpMapiSup_
  
> no Ponteiro opcional para um objeto de suporte MAPI que um provedor de serviços pode usar para chamar os métodos da interface [IMAPISupport: IUnknown](imapisupportiunknown.md) . 
    
_lpStg_
  
> [in, out] Ponteiro para um objeto **IStorage** do OLE que está aberto e tem permissão somente leitura ou leitura/gravação. Como o **IMessage** não oferece suporte a acesso somente gravação, o **OpenIMsgOnIStg** não aceita um objeto de armazenamento aberto no modo somente gravação. 
    
_lpfMsgCallRelease_
  
> no Ponteiro opcional para uma função de retorno de chamada baseada no protótipo [MSGCALLRELEASE](msgcallrelease.md) que o MAPI deve chamar seguindo o último lançamento no objeto **IMessage**-on- **IStorage** . 
    
_ulCallerData_
  
> no Dados do chamador salvos por MAPI com o objeto **IMessage**-on- **IStorage** e passados para a função de retorno de chamada baseada no **MSGCALLRELEASE** . Os dados fornecem contexto sobre o objeto **IMessage** que está sendo liberado e o objeto **IStorage** na parte superior da qual foi criado. 
    
_ulFlags_
  
> no Bitmask dos sinalizadores usados para controlar se o método OLE **IStorage:: Commit** é chamado quando o aplicativo cliente ou provedor de serviços chama o método **IMessage:: SaveChanges** . Os seguintes sinalizadores podem ser definidos: 
    
IMSG_NO_ISTG_COMMIT 
  
> O método OLE **IStorage:: Commit** não deve ser chamado quando o cliente ou provedor chama [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Permite a criação de arquivos Unicode. msg. O arquivo [IMessage](imessageimapiprop.md) resultante mostra STORE_UNICODE_OK em seu [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) e oferece suporte a Propriedades Unicode. 
    
  > [!NOTE]
  > O sinalizador MAPI_UNICODE só tem suporte nesta função no Outlook 2003 ou superior. 
  
_lppMsg_
  
> bota Ponteiro para um ponteiro para o objeto **IMessage** aberto. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados em objetos Property, ou seja, objetos que implementam a interface [IMAPIProp: IUnknown](imapipropiunknown.md) . Para disponibilizar as propriedades MAPI em um objeto de armazenamento estruturado OLE, **OpenIMsgOnIStg** cria um objeto [IMessage: IMAPIProp](imessageimapiprop.md) na parte superior do objeto OLE **IStorage** . Os atributos de propriedade desses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com o [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Uma sessão de mensagens deve ser aberta com O [OpenIMsgSession](openimsgsession.md) antes que **OpenIMsgOnIStg** seja chamado. O fornecimento de um parâmetro _lpMsgSess_ válido garante que a nova mensagem seja criada dentro de uma sessão de mensagem para que ela seja fechada quando a sessão for fechada. Se _lpMsgSess_ for nulo, a mensagem será criada independentemente de qualquer sessão de mensagem. Se o aplicativo cliente ou provedor de serviços que criou a mensagem não o liberar, bem como todos os seus anexos e tabelas abertas, a memória será vazada e poderá fazer com que o aplicativo seja encerrado. 
  
MAPI usa as funções apontadas por _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria da alocação de memória e desalocação, em particular para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto como [IMAPIProp::](imapiprop-getprops.md) GetProps e IMAPITable [:: QueryRows](imapitable-queryrows.md). Os ponteiros _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ são opcionais quando a função **OpenIMsgOnIStg** é chamada com um parâmetro _lpMapiSup_ válido. 
  
Como está lidando com um objeto OLE subjacente, o MAPI também precisa usar a alocação de memória OLE. Para obter mais informações sobre objetos de armazenamento estruturados OLE e alocação de memória OLE, consulte a _referência do programador de OLE_. 
  
Se for fornecido um valor válido para _lpMapiSup_, **IMessage** oferece suporte aos sinalizadores MAPI_DIALOG e ATTACH_DIALOG chamando o método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para fornecer uma interface de usuário de progresso para o [IMAPIProp:: CopyTo](imapiprop-copyto.md) e [IMessage::D eleteattach](imessage-deleteattach.md) métodos. Além disso, o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) tenta converter identificadores de entrada de curto prazo para identificadores de entrada de longo prazo chamando o método [IMAPISupport:: OpenAddressBook](imapisupport-openaddressbook.md) e fazendo chamadas no objeto do catálogo de endereços resultante. Se NULL for passado para _lpMapiSup_, **IMESSAGE** ignorará MAPI_DIALOG e ATTACH_DIALOG e armazenará identificadores de entrada de curto prazo sem conversão. 
  
O objeto **IStorage** apontado pelo parâmetro _lpStg_ deve ser aberto no modo STGM_READ ou STGM_READWRITE. Se o modo STGM_READWRITE for usado, o modo STGM_TRANSACTED também deverá ser definido. 
  
A função de retorno de chamada indicada pelo parâmetro _lpfMsgCallRelease_ é opcional; se fornecido, ele deve se basear no protótipo de função [MSGCALLRELEASE](msgcallrelease.md) . A interface **IMessage** a chama quando a contagem de referência do objeto **IMessage**-on- **IStorage** é definida como zero pela última chamada para seu método de **lançamento** . A função de retorno de chamada é comumente usada para liberar a interface **IStorage** subjacente. O **IMessage** não tentará acessar o objeto **IStorage** apontado pelo parâmetro _lpStg_ depois de fazer o retorno de chamada. 
  
Alguns clientes ou provedores podem gravar dados adicionais no objeto **IStorage** além do que o próprio **IMessage** grava quando o método [SaveChanges](imapiprop-savechanges.md) é chamado. O cliente ou provedor pode usar o sinalizador IMSG_NO_ISTG_COMMIT para impedir que o **IMessage** chame o método OLE **IStorage:: Commit** durante o processamento de uma chamada **SaveChanges** ; Nesse caso, o cliente ou provedor deve confirmar o objeto **IStorage** quando os dados adicionais são gravados. Para ajudar nesse caso, a implementação do **IMessage** garante o nome de todos os subarmazenamentos que ele cria no objeto **IStorage** , começando com a cadeia de caracteres "_ _", ou seja, com dois sublinhados. O cliente ou provedor pode evitar colisões de nome mantendo seus nomes de subarmazenamento desse namespace. 
  
O MAPI não define o comportamento de várias operações abertas realizadas em um subobjeto de uma mensagem, como um anexo, um fluxo ou uma mensagem incorporada. No momento, o MAPI permite que um subobjeto que já esteja aberto para ser aberto mais uma vez, mas o MAPI execute a operação de abertura ao incrementar a contagem de referência para o objeto Open existente e devolvê-lo ao cliente ou provedor que chamou o [IMessage:: OpenAttach ](imessage-openattach.md)ou [IMAPIProp::](imapiprop-openproperty.md) método OpenProperty. Isso significa que o acesso solicitado para a primeira operação aberta em um subobjeto é o acesso fornecido para todas as operações abertas subsequentes, independentemente do acesso solicitado pelas operações. 
  
O procedimento correto para colocar uma mensagem em um anexo é chamar o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) com um identificador de interface de IID_IMessage. **** O OpenProperty atualmente também oferece suporte à criação de anexos de mensagens disponíveis diretamente na interface **IStorage** do OLE, ou seja, usando o identificador de interface IID_IStorage. O acesso ao **IStorage** é suportado para permitir uma maneira fácil de colocar um documento do Microsoft Word em um anexo sem convertê-lo em ou a partir da interface de **IStream** do OLE. No enTanto, **IMessage** pode não se comportar de forma previsível se **OpenIMsgOnIStg** for passado um ponteiro **IStorage** para os dados de anexo e os objetos forem liberados na ordem errada. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Arquivo. cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI usa o método **OpenIMsgOnIStg** para abrir uma interface de IMessage na parte superior do. MSG para que o arquivo possa ser manipulado com MAPI.  <br/> |
   
## <a name="see-also"></a>Confira também

- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)


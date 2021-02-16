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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406518"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um novo [objeto IMessage](imessageimapiprop.md) sobre um objeto **IStorage** OLE existente, a ser usado em uma sessão de mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Imessage.h  <br/> |
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
  
> [in] Ponteiro para um objeto de sessão de mensagem dentro do qual o novo objeto **IMessage** **-on-IStorage** deve ser criado. 
    
_lpAllocateBuffer_
  
> [in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória. 
    
_lpAllocateMore_
  
> [in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional. 
    
_lpFreeBuffer_
  
> [in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória. 
    
_lpMalloc_
  
> [in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.** A interface **IMessage** precisa usar esse método de alocação ao trabalhar com interfaces como **IStorage** e **IStream**. 
    
_lpMapiSup_
  
> [in] Ponteiro opcional para um objeto de suporte MAPI que um provedor de serviços pode usar para chamar os métodos da interface [IMAPISupport : IUnknown.](imapisupportiunknown.md) 
    
_lpStg_
  
> [in, out] Ponteiro para um objeto **IStorage** OLE que está aberto e tem permissão somente leitura ou leitura/gravação. Como **o IMessage** não dá suporte ao acesso somente gravação, **o OpenIMsgOnIStg** não aceita um objeto de armazenamento aberto no modo somente gravação. 
    
_lpfMsgCallRelease_
  
> [in] Ponteiro opcional para uma função de retorno de chamada com base no protótipo [MSGCALLRELEASE](msgcallrelease.md) que o MAPI deve chamar seguindo a última versão no objeto **IMessage**-on-IStorage.  
    
_ulCallerData_
  
> [in] Dados do chamador salvos por MAPI com o objeto **IMessage** **-on-IStorage** e passados para a função de retorno de chamada baseada em **MSGCALLRELEASE.** Os dados proporcionam contexto sobre o objeto **IMessage** que está sendo liberado e o objeto **IStorage** sobre o qual ele foi criado. 
    
_ulFlags_
  
> [in] Bitmask de sinalizadores usados para controlar se o método **OLE IStorage::Commit** é chamado quando o aplicativo cliente ou provedor de serviços chama o método **IMessage::SaveChanges.** Os sinalizadores a seguir podem ser definidos: 
    
IMSG_NO_ISTG_COMMIT 
  
> O método OLE **IStorage::Commit** não deve ser chamado quando o cliente ou provedor chamar [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Habilita a criação de arquivos .msg Unicode. O arquivo [IMessage](imessageimapiprop.md) resultante mostra STORE_UNICODE_OK em sua [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) e dá suporte a propriedades Unicode. 
    
  > [!NOTE]
  > The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher. 
  
_lppMsg_
  
> [out] Ponteiro para um ponteiro para o objeto **IMessage** aberto. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados em objetos de propriedade, ou seja, objetos que implementam o [IMAPIProp : interface IUnknown.](imapipropiunknown.md) Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, **OpenIMsgOnIStg** cria um [IMessage : objeto IMAPIProp](imessageimapiprop.md) sobre o objeto **IStorage** OLE. Os atributos de propriedade nesses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Uma sessão de mensagem deve ser aberta com [OpenIMsgSession](openimsgsession.md) antes de **OpenIMsgOnIStg** ser chamado. Fornecer um parâmetro  _lpMsgSess_ válido garante que a nova mensagem seja criada dentro de uma sessão de mensagem para que ela seja fechada quando a sessão for fechada. Se  _lpMsgSess_ for NULL, a mensagem será criada independentemente de qualquer sessão de mensagem. Se o aplicativo cliente ou provedor de serviços que criou a mensagem não a liberar, bem como todos os seus anexos e tabelas abertas, a memória será vazada e poderá fazer com que o aplicativo seja encerrado. 
  
MAPI uses the functions pointed to  _by lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such [as IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md). Os  _ponteiros lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ são opcionais quando a função **OpenIMsgOnIStg** é chamada com um parâmetro  _lpMapiSup_ válido. 
  
Como ele está lidando com um objeto OLE subjacente, o MAPI também precisa usar a alocação de memória OLE. Para obter mais informações sobre objetos de armazenamento estruturado OLE e alocação de memória OLE, consulte a _Referência do programador OLE._ 
  
Se um valor válido for fornecido para _lpMapiSup_, **IMessage** suportará os sinalizadores MAPI_DIALOG e ATTACH_DIALOG chamando o método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para fornecer uma interface de usuário de progresso para os métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMessage::D eleteAttach.](imessage-deleteattach.md) Além disso, o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) tenta converter identificadores de entrada de curto prazo em identificadores de entrada de longo prazo chamando o método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) e fazendo chamadas no objeto de agendamento de endereço resultante. Se NULL for passado para  _lpMapiSup_, **IMessage** ignorará MAPI_DIALOG e ATTACH_DIALOG e armazenará identificadores de entrada de curto prazo sem conversão. 
  
O **objeto IStorage** apontado pelo parâmetro  _lpStg_ deve ser aberto no modo de STGM_READ ou STGM_READWRITE. Se o STGM_READWRITE padrão for usado, o modo STGM_TRANSACTED também deverá ser definido. 
  
A função de retorno de chamada apontada pelo _parâmetro lpfMsgCallRelease_ é opcional; se fornecido, ele deve ser baseado no protótipo [de função MSGCALLRELEASE.](msgcallrelease.md) A interface **IMessage** a chama quando a contagem de referência do objeto **IMessage**-on-IStorage é definida como zero pela última chamada para seu **método Release.**  A função de retorno de chamada normalmente é usada para liberar a interface **IStorage** subjacente. **IMessage** não tentará acessar o objeto **IStorage** apontado pelo parâmetro  _lpStg_ depois de fazer o retorno de chamada. 
  
Alguns clientes ou provedores podem gravar dados adicionais no objeto **IStorage** além do que o **próprio IMessage** grava quando seu [método SaveChanges](imapiprop-savechanges.md) é chamado. O cliente ou provedor pode usar o sinalizador IMSG_NO_ISTG_COMMIT para impedir que **IMessage** chame o método **OLE IStorage::Commit** durante o processamento de uma **chamada SaveChanges;** nesse caso, o cliente ou provedor deve próprio comprometer o **objeto IStorage** quando os dados adicionais são gravados. Para ajudar nisso, a implementação **IMessage** garante nomear todas as substorages que cria no objeto **IStorage** começando com a cadeia de caracteres "__", ou seja, com dois sublinhados. O cliente ou provedor pode evitar colisões de nomes mantendo seus nomes de substoragem fora desse namespace. 
  
O MAPI não define o comportamento de várias operações abertas executadas em um subobjeto de uma mensagem, como um anexo, um fluxo ou uma mensagem incorporada. MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method. Isso significa que o acesso solicitado para a primeira operação de abertura em um subobjeto é o acesso fornecido para todas as operações abertas subsequentes, independentemente do acesso solicitado pelas operações. 
  
O procedimento correto para colocar uma mensagem em um anexo é chamar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com um identificador de interface de IID_IMessage. **OpenProperty** atualmente também oferece suporte à criação de anexos de mensagem disponíveis diretamente na interface **IStorage** OLE, ou seja, usando o identificador IID_IStorage interface. **O acesso a IStorage** é suportado para permitir uma maneira fácil de colocar um documento do Microsoft Word em um anexo sem convertê-lo para ou da interface **IStream** OLE. No entanto, **IMessage** pode não se comportar de forma previsível se **OpenIMsgOnIStg** for passado um ponteiro **IStorage** para os dados do anexo e, em seguida, os objetos são liberados na ordem errada. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI usa **o método OpenIMsgOnIStg** para abrir uma interface IMessage sobre o . Arquivo MSG para que o arquivo possa ser manipulado com MAPI.  <br/> |
   
## <a name="see-also"></a>Confira também

- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)


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
ms.openlocfilehash: 56e663ced33da933b4276911b609f2fae1c5d78e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563959"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um novo objeto [IMessage](imessageimapiprop.md) na parte superior de um objeto OLE **IStorage** existente, a ser usado em uma sessão de mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] Ponteiro para um objeto de sessão de mensagem dentro do qual o novo **IMessage**objeto **|** - on - deve ser criada. 
    
_lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
_lpAllocateMore_
  
> [in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional. 
    
_lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
_lpMalloc_
  
> [in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** . A interface **IMessage** deve usar esse método de alocação ao trabalhar com interfaces como **IStorage** e **IStream**. 
    
_lpMapiSup_
  
> [in] Opcional ponteiro para um objeto de suporte MAPI que um provedor de serviços pode usar para chamar os métodos para o [IMAPISupport: IUnknown](imapisupportiunknown.md) interface. 
    
_lpStg_
  
> [além, out] Ponteiro para um objeto OLE **IStorage** que está aberta e somente leitura ou permissão de leitura/gravação. Porque **IMessage** não oferece suporte para acesso somente gravação, **OpenIMsgOnIStg** não aceita um objeto de armazenamento aberto no modo somente gravação. 
    
_lpfMsgCallRelease_
  
> [in] Ponteiro opcional para uma função de retorno de chamada com base em protótipo [MSGCALLRELEASE](msgcallrelease.md) que MAPI deve chamar após a última versão em **IMessage**o objeto **|** - on. 
    
_ulCallerData_
  
> [in] Dados do chamador salvo pelo MAPI com o objeto **|** **IMessage**- on - e passado para o **MSGCALLRELEASE** com base em função de retorno de chamada. Os dados fornecem contexto sobre o objeto **IMessage** está sendo liberado e o objeto **|** na parte superior de qual ele foi criado. 
    
_ulFlags_
  
> [in] Bitmask dos sinalizadores utilizada para controlar se o método OLE **IStorage::Commit** é chamado quando o aplicativo cliente ou o provedor de serviço chama o método **IMessage::SaveChanges** . Sinalizadores a seguir podem ser definidos: 
    
IMSG_NO_ISTG_COMMIT 
  
> O método OLE **IStorage::Commit** não deve ser chamado quando o cliente ou o provedor chama [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Permite a criação de arquivos do. msg Unicode. O arquivo resultante de [IMessage](imessageimapiprop.md) mostra STORE_UNICODE_OK no seu [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) e oferece suporte a Unicode propriedades. 
    
  > [!NOTE]
  > O sinalizador MAPI_UNICODE somente há suporte para essa função no Outlook 2003 ou superior. 
  
_lppMsg_
  
> [out] Ponteiro para um ponteiro para o objeto **IMessage** aberto. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Atributos de propriedade só podem ser acessados na propriedade objetos, ou seja, objetos Implementando o [IMAPIProp: IUnknown](imapipropiunknown.md) interface. Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, **OpenIMsgOnIStg** cria um [IMessage: IMAPIProp](imessageimapiprop.md) objeto na parte superior do objeto OLE **IStorage** . Os atributos de propriedade nesses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Uma sessão de mensagem deve ser aberta com [OpenIMsgSession](openimsgsession.md) antes de **OpenIMsgOnIStg** é chamado. Fornecendo um parâmetro válido _lpMsgSess_ fazer sures a nova mensagem é criada dentro de uma sessão de mensagem, de modo que ela é fechada quando a sessão é fechada. Se _lpMsgSess_ for NULL, a mensagem é criada, independentemente de qualquer sessão de mensagens. Se o aplicativo cliente ou o provedor de serviço que criou a mensagem não liberar a ele, bem como todos os seus respectivos anexos e abrir tabelas, memória tenha vazada e pode causar o aplicativo seja finalizado. 
  
O MAPI usa as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação, especificamente para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). Os ponteiros _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ são opcionais quando a função **OpenIMsgOnIStg** é chamada com um parâmetro válido _lpMapiSup_ . 
  
Porque ele está lidando com um objeto OLE subjacente, MAPI também precisa usar a alocação de memória do OLE. Para obter mais informações sobre objetos de armazenamento estruturado OLE e alocação de memória do OLE, consulte a _referência do programador do OLE_. 
  
Se um valor válido é fornecido para _lpMapiSup_, **IMessage** suporta os sinalizadores MAPI_DIALOG e ATTACH_DIALOG chamando o método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para fornecer uma interface do usuário de andamento para o [IMAPIProp::CopyTo](imapiprop-copyto.md) e os métodos [IMessage::DeleteAttach](imessage-deleteattach.md) . Além disso, o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) tenta converter a curto prazo identificadores de entrada aos identificadores de entrada de longo prazo chamando o método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) e fazendo chamadas sobre o objeto resultante de catálogo de endereços. Se NULL é passado para _lpMapiSup_, **IMessage** ignora MAPI_DIALOG e ATTACH_DIALOG e armazena os identificadores de entrada de curto prazo sem a conversão. 
  
O objeto **|** apontado pelo parâmetro _lpStg_ deve ser aberto no modo de STGM_READ ou STGM_READWRITE. Se o modo STGM_READWRITE for usado, o modo STGM_TRANSACTED também deve ser definido. 
  
A função de retorno de chamada apontada pelo parâmetro _lpfMsgCallRelease_ é opcional. Se for fornecido, ele deve se basear o protótipo de função [MSGCALLRELEASE](msgcallrelease.md) . A interface **IMessage** chame quando a contagem de referência do objeto **IMessage**- on - **IStorage** está definida como zero pela última chamada para seu método de **lançamento** . A função de retorno de chamada geralmente é usada para liberar a interface **IStorage** subjacente. **IMessage** não tentará acessar o objeto **|** apontado pelo parâmetro _lpStg_ depois de fazer o retorno de chamada. 
  
Alguns clientes ou provedores podem gravar dados adicionais para o objeto **|** além quais **IMessage** próprio grava quando seu método [SaveChanges](imapiprop-savechanges.md) é chamado. O cliente ou o provedor pode usar o sinalizador IMSG_NO_ISTG_COMMIT para impedir que **IMessage** chamar o método OLE **IStorage::Commit** durante o processamento de uma chamada **SaveChanges** ; Neste caso o cliente ou o provedor deve próprio confirmar o objeto **|** quando os dados adicionais serão gravados. Para ajudar nisso, a implementação de **IMessage** garante nomear substorages todos, que ele cria o objeto **|** começando com a cadeia de caracteres _", ou seja, com dois sublinhados. O cliente ou o provedor pode evitar conflitos de nome, mantendo os nomes de suas subarmazenamento sem esse namespace. 
  
MAPI não define o comportamento das operações de abrir vários realizadas em um Subobjeto de uma mensagem, como um anexo, um fluxo ou uma mensagem incorporada. MAPI atualmente permite um Subobjeto que já está aberto para ser aberto mais uma vez, mas MAPI executa a operação aberta com incrementar a contagem de referência para o objeto aberto existente e retorná-lo para o cliente ou o provedor que chamou o [IMessage::OpenAttach ](imessage-openattach.md)ou método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Isso significa que o acesso solicitado para a operação de abertura primeira em um Subobjeto é o acesso fornecido para todas as operações de abrir subsequentes, independentemente do acesso solicitado pelas operações. 
  
O procedimento correto para a inserção de uma mensagem em um anexo é chamar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com um identificador de interface de IID_IMessage. **OpenProperty** atualmente também dá suporte à criação de anexos de mensagens disponíveis diretamente na interface OLE **IStorage** , ou seja, usando o identificador de interface IID_IStorage. Acesso de **IStorage** é suportado para permitir uma maneira fácil de colocar um documento do Microsoft Word em um anexo sem convertê-lo ou para a interface **IStream** do OLE. No entanto, **IMessage** podem não se comportar previsibilidade se **OpenIMsgOnIStg** é passado um ponteiro **IStorage** para os dados do anexo e, em seguida, os objetos são lançados na ordem errada. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|CPP  <br/> |LoadMSGToMessage  <br/> |MFCMAPI usa o método **OpenIMsgOnIStg** para abrir uma interface IMessage na parte superior do. MSG de arquivo para que o arquivo pode ser manipulado com MAPI.  <br/> |
   
## <a name="see-also"></a>Confira também

- [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)


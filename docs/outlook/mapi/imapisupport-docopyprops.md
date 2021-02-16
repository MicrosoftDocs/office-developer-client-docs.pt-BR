---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405580"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move uma ou mais propriedades de um objeto para outro objeto.
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _lpSrcInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o objeto com as propriedades a serem copiadas ou movidas.
    
 _lpSrcObj_
  
> [in] Um ponteiro para o objeto que contém as propriedades a serem copiadas ou movidas.
    
 _lpIncludeProps_
  
> [in] Um ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz contada de marcas de propriedade que indicam as propriedades a ser copiadas ou movimentadas. O  _parâmetro lpIncludeProps_ não pode ser NULL. 
    
 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso.
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação de um indicador de progresso. Se NULL for passado no  _parâmetro lpProgress,_ o indicador de progresso será exibido usando a implementação de MAPI. O _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG seja definido no _parâmetro ulFlags._ 
    
 _lpDestInterface_
  
> [in] Um ponteiro para o identificador da interface que representa a interface a ser usada para acessar o objeto e receber as propriedades que são copiadas ou movidas.
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a operação de cópia ou movimentação é executada. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **DoCopyProps** deve executar uma operação de movimentação em vez de uma operação de cópia. Quando esse sinalizador não está definido, **o DoCopyProps** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> As propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não estiver definido, **DoCopyProps** substituirá as propriedades existentes. 
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro para um ponteiro para uma [estrutura SPropProblemArray;](spropproblemarray.md) caso contrário, NULL, que indica nenhuma necessidade de informações de erro. Se  _lppProblems_ for um ponteiro válido na entrada, **DoCopyProps** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Uma propriedade a ser copiada ou movida já existe no objeto de destino e o MAPI_NOREPLACE sinalizador está definido. 
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem contém direta ou indiretamente o objeto de destino. Um trabalho significativo pode ter sido realizado antes dessa condição ser descoberta, portanto, os objetos de origem e destino podem ser parcialmente modificados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface identificada pelo parâmetro  _lpSrcInterface_ não é suportada pelo objeto de origem ou a interface identificada pelo parâmetro  _lpDestInterface_ não é suportada pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.
    
Os seguintes valores podem ser retornados na **estrutura SPropProblemArray,** mas não como valores de retorno para **DoCopyProps**. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE padrão foi definido e **DoCopyProps** não dá suporte a Unicode ou MAPI_UNICODE não foi definido e **DoCopyProps** dá suporte apenas a Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino. Este erro não é grave; o chamador deve permitir que a operação de cópia continue.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo que o chamador espera.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::D oCopyProps** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens podem chamar **DoCopyProps** para implementar o método [IMAPIProp::CopyProps](imapiprop-copyprops.md) para suas pastas e mensagens. **DoCopyProps** copia ou move as propriedades identificadas na matriz de marca de propriedade apontada por  _lpIncludeProps_ e que estão presentes no objeto apontado por  _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando você copia propriedades entre objetos do mesmo tipo, como duas mensagens, os parâmetros  _lpSrcInterface_ e  _lpDestInterface_ devem conter o mesmo identificador de interface, e os parâmetros  _lpSrcObj_ e  _lpDestObj_ devem apontar para objetos do mesmo tipo. Se  _lpDestInterface_ for definido como NULL, **DoCopyProps** retornará MAPI_E_INVALID_PARAMETER. Se você definir  _lpDestInterface_ como um identificador de interface aceitável, mas definir  _lpDestObj_ como um ponteiro inválido, os resultados serão imprevisíveis. Provavelmente, seu provedor falhará. 
  
De definida MAPI_NOREPLACE sinalizador se você não quiser que nenhuma das propriedades no objeto de destino seja substituída. As propriedades no objeto de destino existentes no objeto de origem e que não são substituídas não são excluídas ou modificadas.
  
Para copiar a lista de destinatários de uma mensagem, inclua a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) na matriz de marca de propriedade apontada pelo parâmetro _lpIncludeProps._ Para copiar os anexos da mensagem, inclua a **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) . 
  
Para copiar a hierarquia ou a tabela de conteúdo de um contêiner de pasta ou de um conjunto de endereços, inclua **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na matriz de marca de propriedade. Para incluir a tabela de conteúdo associada de uma pasta, inclua a propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) na matriz.
  
Se as subpastas são copiadas ou movidas, seus conteúdos são copiados ou movidos em sua totalidade, independentemente do uso das propriedades indicadas pela **estrutura SPropTagArray.** 
  
 **O DoCopyProps** relata erros globais que ocorrem com a operação como um todo e erros individuais que ocorrem com uma ou mais das propriedades. Esses erros individuais são colocados em uma **estrutura SPropProblemArray.** Você pode suprimir o relatório de erros no nível da propriedade passando NULL, em vez de um ponteiro válido, para o parâmetro de estrutura da matriz do problema de propriedade. 
  
Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems._ Quando **DoCopyProps** retornar S_OK, verifique se há possíveis erros com propriedades individuais na estrutura. Quando **DoCopyProps** retorna um erro, nenhuma informação é retornada na **estrutura SPropProblemArray.** Em vez disso, chame [o método IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **DoCopyProps** retornar S_OK, livre a estrutura **SPropProblemArray** retornada chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônica PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propriedade canônica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


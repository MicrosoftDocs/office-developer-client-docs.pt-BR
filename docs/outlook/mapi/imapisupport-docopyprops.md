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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c93e01b1e4621cddc4c98d528e5f5339cba21dae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767224"
---
# <a name="imapisupportdocopyprops"></a>IMAPISupport::DoCopyProps

  
  
**Aplica-se a**: Outlook 
  
Copia ou move uma ou mais propriedades de um objeto para um outro objeto.
  
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

## <a name="parameters"></a>Par�metros

 _lpSrcInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o objeto com as propriedades devem ser copiados ou movidos.
    
 _lpSrcObj_
  
> [in] Um ponteiro para o objeto que contém as propriedades para ser copiados ou movidos.
    
 _lpIncludeProps_
  
> [in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz contada das marcas de propriedade que indicam as propriedades para copiar ou mover. O parâmetro _lpIncludeProps_ não pode ser NULL. 
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso.
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação de um indicador de progresso. Se o parâmetro _lpProgress_ é passado NULL, o indicador de progresso é exibido, usando a implementação de MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpDestInterface_
  
> [in] Um ponteiro para o identificador de interface que representa a interface que será usada para acessar o objeto para receber as propriedades que são copiadas ou movidas.
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a operação de cópia ou movimentação é executada. Sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **DoCopyProps** deve realizar uma operação de movimentação, em vez de uma operação de cópia. Quando esse sinalizador não estiver definida, **DoCopyProps** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> Propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não estiver definida, **DoCopyProps** substitui as propriedades existentes. 
    
 _lppProblems_
  
> [além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, NULL, que indica que não há necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **DoCopyProps** retorna informações detalhadas sobre erros no copiando uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Uma propriedade devem ser copiados ou movidos já existe no objeto de destino e o sinalizador MAPI_NOREPLACE está definido. 
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem direta ou indiretamente contém o objeto de destino. Trabalho significativo pode ter sido executado antes que esta condição foi descoberta, para que os objetos de origem e destino podem ser modificados parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Não há suporte para a interface identificada pelo parâmetro _lpSrcInterface_ pelo objeto de origem ou não há suporte para a interface identificada pelo parâmetro _lpDestInterface_ pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino é o mesmo que o objeto de origem.
    
Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **DoCopyProps**. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e **DoCopyProps** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **DoCopyProps** suporta somente Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque ele é uma propriedade somente leitura, computada pelo proprietário do objeto de destino. Esse erro não é grave; o chamador deve permitir que a operação de cópia continuar.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado do chamador.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::DoCopyProps** é implementado para objetos de suporte do provedor de repositório de mensagem. Provedores de armazenamento de mensagens podem chamar **DoCopyProps** para implementar o método [IMAPIProp::CopyProps](imapiprop-copyprops.md) para suas pastas e mensagens. **DoCopyProps** copia ou move as propriedades que são identificados na propriedade tag matriz apontado pela _lpIncludeProps_ e que estão presentes no objeto apontado pela _lpSrcObj_. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando você copia propriedades entre os objetos do mesmo tipo, como duas mensagens, os parâmetros _lpSrcInterface_ e _lpDestInterface_ devem conter os mesmos parâmetros de identificador e _lpSrcObj_ e _lpDestObj_ de interface deve apontar para objetos do mesmo tipo. Se _lpDestInterface_ for definido como NULL, **DoCopyProps** retorna MAPI_E_INVALID_PARAMETER. Se você definir _lpDestInterface_ como um identificador de interface aceitável, mas set _lpDestObj_ para um ponteiro inválido, os resultados serão imprevisíveis. Mais provável seu provedor irá falhar. 
  
Defina o sinalizador MAPI_NOREPLACE se você não quiser que qualquer uma das propriedades no objeto de destino a ser substituído. Propriedades no objeto de destino que existem no objeto de origem e não são sobrescritas não são excluídas ou modificadas.
  
Para copiar a lista de destinatários da mensagem, inclua a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) na matriz de marca de propriedade apontado pelo parâmetro _lpIncludeProps_ . Para copiar os anexos da mensagem, inclua a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar uma pasta, a hierarquia do contêiner de catálogo de endereços ou a tabela de conteúdo, inclua **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na matriz de marca de propriedade. Para incluir a tabela de conteúdo associado de uma pasta, inclua a propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) na matriz.
  
Se as subpastas são copiadas ou movidas, seus conteúdos são copiados ou movidos na íntegra, independentemente do uso das propriedades indicados pela estrutura **SPropTagArray** . 
  
 **DoCopyProps** relatórios individuais erros que ocorrem com uma ou mais das propriedades e globais erros que ocorrem com a operação como um todo. Esses erros individuais são colocados em uma estrutura **SPropProblemArray** . Você pode suprimir relatório no nível de propriedade passando NULL, em vez de um ponteiro válido, para o parâmetro de estrutura de matriz de problema de propriedade de erros. 
  
Se você desejar receber informações sobre erros, passe um ponteiro de estrutura de **SPropProblemArray** válido no parâmetro _lppProblems_ . Quando **DoCopyProps** Retorna S_OK, verifique se há erros possíveis com as propriedades individuais na estrutura. Quando **DoCopyProps** retornará um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** . Em vez disso, chame o método [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **DoCopyProps** Retorna S_OK, livre a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::CopyProps](imapiprop-copyprops.md)
  
[IMAPISupport::CopyMessages](imapisupport-copymessages.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[Propriedade canônico de PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônico de PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônico de PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propriedade canônico de PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônico de PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


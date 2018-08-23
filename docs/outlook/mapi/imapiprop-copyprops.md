---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ee6fcaf2fa168f6be91b798efa249799f738bfa0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571077"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cópias ou movimentações de propriedades selecionadas. 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _lpIncludeProps_
  
> [in] Um ponteiro para uma matriz de marca de propriedade que especifica as propriedades para copiar ou mover. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não podem ser incluídos na matriz. O parâmetro _lpIncludeProps_ não pode ser **Nulo**.
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação de um indicador de progresso. Se **Nulo** é passado no parâmetro _lpProgress_ , o indicador de progresso é exibido, usando a implementação de MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que deve ser usada para acessar o objeto apontado pelo parâmetro _lpDestObj_ . O parâmetro _lpInterface_ não deve ser **nula**.
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a operação de cópia ou movimentação. Sinalizadores a seguir podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Se **CopyProps** chama o método [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) para lidar com a cópia ou a operação de movimentação, ele em vez disso, deve retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY. O sinalizador MAPI_DECLINE_OK é definido por MAPI para limitar a recursão. Os clientes não definir esse sinalizador. 
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **CopyProps** deve realizar uma operação de movimentação, em vez de uma operação de cópia. Quando esse sinalizador não estiver definida, **CopyProps** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> Propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não estiver definida, **CopyProps** substitui as propriedades existentes. 
    
 _lppProblems_
  
> [além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, **null**, indicando que não há nenhuma necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **CopyProps** retorna informações detalhadas sobre erros no copiando uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Propriedades foi copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Não é possível copiar um Subobjeto porque já existe um Subobjeto com o mesmo nome de exibição, definido pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), no objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> O provedor de serviços não implementa a operação de cópia.
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem executando a operação de cópia ou movimentação direta ou indiretamente contém o objeto de destino. Trabalho significativo pode ter sido executado antes que esta condição foi descoberta, para que os objetos de origem e destino podem ser modificados parcialmente. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Não há suporte para a interface identificada pelo parâmetro _lpInterface_ pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino é o mesmo que o objeto de origem.
    
Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **CopyProps**. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e **CopyProps** não oferece suporte a Unicode, ou MAPI_UNICODE não foi definido e **CopyProps** suporta somente Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque ele é uma propriedade somente leitura, computada pelo proprietário do objeto de destino. Esse erro não é grave; o chamador deve permitir que a operação de cópia continuar.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::CopyProps** copia ou move propriedades selecionadas do objeto atual para um objeto de destino. **CopyProps** é usado principalmente para responder e encaminhar mensagens, onde apenas algumas das propriedades da mensagem original com a resposta de viagem ou encaminhadas a cópia. 
  
Qualquer subobjetos no objeto de origem automaticamente estão incluídos na operação e copiados ou movidos na íntegra, independentemente do uso das propriedades indicados pela estrutura [SPropTagArray](sproptagarray.md) . Por padrão, **CopyProps** substitui quaisquer propriedades no objeto de destino que corresponde às propriedades do objeto de origem. Se qualquer uma das propriedades movidas ou copiadas já existir no objeto de destino, as propriedades existentes são sobrescritas por novas propriedades, exceto se o sinalizador MAPI_NOREPLACE estiver definido no parâmetro _ulFlags_ . As informações existentes no objeto de destino que não será substituído são permanecem inalteradas. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode fornecer uma implementação total de **CopyProps** ou baseiam-se na implementação de MAPI fornece em seu objeto de suporte. Se você quiser usar a implementação de MAPI, chame o método de **IMAPISupport::DoCopyProps** . No entanto, se você delega o processamento para **DoCopyProps** e você é passadas o sinalizador MAPI_DECLINE_OK, evitar a chamada de suporte e retornar MAPI_E_DECLINE_COPY em vez disso. Você será chamado com esse sinalizador por MAPI para evitar a recursão possível que pode ocorrer quando você copia pastas. 
  
Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso. Use a implementação de [IMAPIProgress](imapiprogressiunknown.md) que é passada no parâmetro _lpProgress_ , se houver uma. Se _lpProgress_ for **nula**, chame o método de [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar a implementação de MAPI. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não definir o sinalizador MAPI_DECLINE_OK; ele é usado pelo MAPI em suas chamadas para a mensagem implementações de **CopyProps** do provedor de repositório. 
  
Porque as operações de movimentação e cópia podem levar o tempo, é recomendável solicitar a exibição de um indicador de progresso, definindo o sinalizador MAPI_DIALOG. Você pode definir o parâmetro _lpProgress_ à sua implementação do **IMAPIProgress**, se você tiver um, ou como **Nulo**. Se _lpProgress_ for **nula**, **CopyProps** usará o indicador de progresso padrão fornecido pelo MAPI. 
  
Você pode suprimir a exibição de um indicador de progresso, não definindo o sinalizador MAPI_DIALOG. **CopyProps** ignorará os parâmetros _ulUIParam_ e _lpProgress_ e evitar exibindo o indicador. 
  
 **CopyProps** possível denunciar global e individual ou erros que ocorrem com uma ou mais das propriedades. Esses erros individuais são colocados em uma estrutura **SPropProblemArray** . Você pode suprimir relatório no nível de propriedade passando **Nulo**, em vez de um ponteiro válido, para o parâmetro de estrutura de matriz de problema de propriedade de erros. 
  
Se você desejar receber informações sobre erros, passe um ponteiro de estrutura de **SPropProblemArray** válido no parâmetro _lppProblems_ . Quando **CopyProps** Retorna S_OK, verifique se há erros possíveis com as propriedades individuais na estrutura. Quando **CopyProps** retornará um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** . Em vez disso, chame o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **CopyProps** Retorna S_OK, livre a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Se você estiver copiando propriedades que são exclusivas para o tipo de objeto de origem, você deve garantir que o objeto de destino é do mesmo tipo. **CopyProps** não impede que você associar propriedades que geralmente pertencem a um tipo de objeto com outro tipo de objeto. Cabe a você copie as propriedades que fazem sentido para o objeto de destino. Por exemplo, você não deve copiar propriedades da mensagem para um contêiner de catálogo de endereços. 
  
Para garantir que você está copiando entre os objetos do mesmo tipo, verifique se o objeto de origem e destino são do mesmo tipo, por comparando ponteiros de objeto ou chamar o método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . Defina o identificador de interface apontado pela _lpInterface_ para a interface padrão para o objeto de origem. Além disso, certifique-se de que o tipo de objeto ou a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é o mesmo para os dois objetos. Por exemplo, se você está copiando uma mensagem, defina _lpInterface_ IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos para MAPI_MESSAGE. 
  
Se um ponteiro inválido é passado no parâmetro _lpDestObj_ , os resultados serão imprevisíveis. 
  
Para copiar a lista de destinatários da mensagem, chame o método **CopyProps** da mensagem e incluir a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) na matriz de marca de propriedade. Para copiar os anexos da mensagem, inclua a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar uma pasta, a hierarquia do contêiner de catálogo de endereços ou a tabela de conteúdo, incluem o **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou propriedades **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) o matriz de marca de propriedade. Para incluir a tabela de conteúdo associado de uma pasta, inclua a propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) na matriz. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI usa o método **IMAPIProp::CopyProps** para copiar propriedades nomeadas de uma mensagem para outro.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI usa o método **IMAPIProp::CopyProps** para colar uma propriedade que foi copiada de outro objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriedade canônica PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propriedade canônica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propriedade canônica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)


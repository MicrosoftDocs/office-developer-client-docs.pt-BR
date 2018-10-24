---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382943"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia uma ou mais entradas, os usuários geralmente mensagens ou listas de distribuição.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpEntries_
  
> [in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que contém os identificadores de entrada das entradas para copiar. 
    
 _ulUIParam_
  
> [in] O identificador para a janela pai de todas as caixas de diálogo ou windows esse método exibe. O parâmetro _ulUIParam_ deve ser zero se o sinalizador AB_NO_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso ou nulo. Se _lpProgress_ for NULL, um indicador de progresso deve ser exibido usando o objeto de progresso fornecido pelo MAPI por meio do método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) . O parâmetro _lpProgress_ será ignorado se o sinalizador AB_NO_DIALOG está definido na _ulFlags_.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a operação de cópia é executada. Sinalizadores a seguir podem ser definidos:
    
AB_NO_DIALOG 
  
> Suprime a exibição de um indicador de progresso. Se esse sinalizador não estiver definida, um indicador de progresso é exibido.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indica que um afastado nível de verificação de entrada duplicada deve ser realizado. A implementação de verificação de entrada duplicada afastada é específico do provedor. Por exemplo, um provedor pode definir uma correspondência afastada conforme qualquer duas entradas que têm o mesmo nome de exibição.
    
CREATE_CHECK_DUP_STRICT 
  
> Indica que um nível estrito de verificação de entrada duplicada deve ser realizado. A implementação de verificação de entrada duplicada strict é específico do provedor. Por exemplo, um provedor pode definir uma correspondência estrita como qualquer duas entradas que têm ambas o mesmo nome e endereço de mensagens são exibidos.
    
CREATE_REPLACE 
  
> Indica que uma nova entrada deve substituir um existente, se for determinado que as duas versões sejam duplicatas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de cópia foi bem-sucedida.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A operação de cópia bem-sucedida, mas um ou mais das entradas não pôde ser copiado. Quando este valor é retornado, a chamada deve ser manipulada com êxito. Para testar esse valor, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IABContainer::CopyEntries** copia entradas do mesmo contêiner ou em um contêiner diferente. Uma chamada para **CopyEntries** é funcionalmente equivalente à fazendo as seguintes chamadas para cada entrada a serem copiados: 
  
1. O método [IABContainer::CreateEntry](iabcontainer-createentry.md) para criar a nova entrada. 
    
2. O método [IMAPIProp::GetProps](imapiprop-getprops.md) para ler as propriedades da entrada a ser copiado. 
    
3. O método [IMAPIProp::SetProps](imapiprop-setprops.md) para gravar as propriedades para a nova entrada. 
    
4. Método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova entrada para executar uma gravação. 
    
5. Método de [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) da nova entrada ao lançamento de referência do contêiner. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Todos os contêineres que suportam o método **IABContainer::CopyEntries** devem ser pode ser modificados. Defina sinalizador AB_MODIFIABLE do seu contêiner na sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ela é modificável. 
  
Você deve oferecer suporte a todos os sinalizadores; No entanto, a interpretação e usar esses sinalizadores é específico da implementação — ou seja, você pode determinar o significado a semântica dos sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT no contexto da sua implementação. Se você não pode ou não determinam se uma entrada é uma duplicata, sempre permita a entrada a ser copiado. 
  
Se o sinalizador CREATE_REPLACE estiver definido, sempre copie a entrada independentemente se CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT é definida e se a entrada é uma duplicata. 
  
Se CREATE_REPLACE não estiver definida e CREATE_CHECK_DUP_STRICT for definido, verificar duplicatas. Se uma entrada é considerada uma duplicata, não copie a entrada. 
  
Não é necessário dar suporte a CREATE_REPLACE; não oferece suporte à CREATE_REPLACE significa que você pode ignorá-la e executar sempre uma cópia. 
  
Retorne o aviso MAPI_W_PARTIAL_COMPLETION somente se uma entrada não duplicada não pode ser copiada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use os sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT para indicar ao provedor de como você deseja que o contêiner para executar a verificação de duplicata-entrada. Se você precisa ter uma entrada adicionada, independentemente se ele é uma duplicata, não defina nenhuma desses sinalizadores ou definir o sinalizador CREATE_REPLACE. CREATE_REPLACE indica que não faz se uma entrada é uma duplicata; Você sempre deseja substituir a entrada original. 
  
## <a name="see-also"></a>Confira também



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


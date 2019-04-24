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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346393"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia uma ou mais entradas, geralmente usuários de mensagens ou listas de distribuição.
  
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
  
> no Um ponteiro para uma matriz de [](entrylist.md) estruturas de ENTRYLIST que contém os identificadores de entrada das entradas a serem copiadas. 
    
 _ulUIParam_
  
> no O identificador para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O parâmetro _ulUIParam_ deve ser zero se o sinalizador AB_NO_DIALOG estiver definido no parâmetro _parâmetroulflags_ . 
    
 _lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso ou nulo. Se _lpProgress_ for NULL, um indicador de progresso deverá ser exibido usando o objeto Progress fornecido pelo MAPI através do método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) . O parâmetro _lpProgress_ será ignorado se o sinalizador AB_NO_DIALOG estiver definido em _parâmetroulflags_.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a operação de cópia é realizada. Os seguintes sinalizadores podem ser definidos:
    
AB_NO_DIALOG 
  
> SuPrime a exibição de um indicador de progresso. Se esse sinalizador não for definido, um indicador de progresso será exibido.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indica que um nível flexível de verificação de entrada duplicada deve ser executado. A implementação da verificação de entrada duplicada resolta é específica do provedor. Por exemplo, um provedor pode definir uma correspondência frouxa como qualquer duas entradas com o mesmo nome de exibição.
    
CREATE_CHECK_DUP_STRICT 
  
> Indica que um nível estrito de verificação de entrada duplicada deve ser executado. A implementação de verificação de entrada duplicada estrita é específica do provedor. Por exemplo, um provedor pode definir uma correspondência estrita como qualquer duas entradas que tenham o mesmo nome de exibição e endereço de mensagens.
    
CREATE_REPLACE 
  
> Indica que uma nova entrada deve substituir uma existente se for determinado que as duas são duplicatas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de cópia foi bem-sucedida.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A operação de cópia foi bem-sucedida, mas uma ou mais entradas não puderam ser copiadas. Quando esse valor é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse valor, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IABContainer:: CopyEntries** copia entradas do mesmo contêiner ou de um contêiner diferente. Uma chamada para **CopyEntries** é funcionalmente equivalente a fazer as seguintes chamadas para cada entrada a ser copiada: 
  
1. O método [IABContainer:: createentry](iabcontainer-createentry.md) para criar a nova entrada. 
    
2. O método [IMAPIProp::](imapiprop-getprops.md) GetProps para ler as propriedades da entrada a ser copiada. 
    
3. O método [IMAPIProp::](imapiprop-setprops.md) SetProps para gravar as propriedades na nova entrada. 
    
4. O método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da nova entrada para executar uma gravação. 
    
5. O método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) da nova entrada para liberar a referência do contêiner. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Todos os contêineres que suportam o método **IABContainer:: CopyEntries** devem ser modificáveis. Defina o sinalizador AB_MODIFIABLE de seu contêiner em sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ele é modificável. 
  
Você deve dar suporte a todos os sinalizadores; no entanto, a interpretação e o uso desses sinalizadores são específicos de implementação, ou seja, você pode determinar o que a semântica dos sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT significam no contexto da sua implementação. Se você não puder ou não determinar se uma entrada é uma duplicata, sempre permita que a entrada seja copiada. 
  
Se o sinalizador CREATE_REPLACE estiver definido, sempre copie a entrada independentemente de o CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT ser definido e se a entrada é uma duplicata. 
  
Se CREATE_REPLACE não estiver definido e CREATE_CHECK_DUP_STRICT estiver definido, verifique se há duplicatas. Se uma entrada for determinada como uma duplicata, não copie a entrada. 
  
Você não precisa suportar o CREATE_REPLACE; não oferecer suporte a CREATE_REPLACE significa que você pode ignorá-lo com segurança e sempre executar uma cópia. 
  
ReTorne o aviso MAPI_W_PARTIAL_COMPLETION somente se não for possível copiar uma entrada não duplicada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use os sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT para indicar ao provedor como você deseja que o contêiner execute a verificação de entrada duplicada. Se for necessário ter uma entrada adicionada independentemente de ser uma duplicata, não defina nenhum desses sinalizadores ou defina o sinalizador CREATE_REPLACE. CREATE_REPLACE indica que você não tem cuidado se uma entrada for uma duplicata; Você sempre deseja que ele substitua a entrada original. 
  
## <a name="see-also"></a>Confira também



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


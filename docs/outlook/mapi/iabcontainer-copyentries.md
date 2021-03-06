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
  
Copia uma ou mais entradas, normalmente usuários de mensagens ou listas de distribuição.
  
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
  
> [in] Um ponteiro para uma matriz de [estruturas ENTRYLIST](entrylist.md) que contém os identificadores de entrada das entradas a ser copiada. 
    
 _ulUIParam_
  
> [in] O alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O _parâmetro ulUIParam_ deve ser zero se o sinalizador AB_NO_DIALOG for definido no _parâmetro ulFlags._ 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso ou NULL. Se _lpProgress_ for NULL, um indicador de progresso deverá ser exibido usando o objeto de progresso fornecido por MAPI por meio do [método IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) O  _parâmetro lpProgress_ será ignorado se o sinalizador AB_NO_DIALOG estiver definido em  _ulFlags_.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a operação de cópia é executada. Os sinalizadores a seguir podem ser definidos:
    
AB_NO_DIALOG 
  
> Suprime a exibição de um indicador de progresso. Se esse sinalizador não estiver definido, um indicador de progresso será exibido.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indica que um nível solto de verificação de entrada duplicada deve ser executado. A implementação da verificação de entrada duplicada livre é específica do provedor. Por exemplo, um provedor pode definir uma combinação livre como qualquer uma das duas entradas que tenham o mesmo nome de exibição.
    
CREATE_CHECK_DUP_STRICT 
  
> Indica que um nível estrito de verificação de entrada duplicada deve ser realizado. A implementação da verificação de entrada duplicada estrita é específica do provedor. Por exemplo, um provedor pode definir uma combinação estrita como qualquer uma das duas entradas que tenham o mesmo nome de exibição e endereço de mensagens.
    
CREATE_REPLACE 
  
> Indica que uma nova entrada deve substituir uma existente se for determinado que as duas são duplicatas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de cópia foi bem-sucedida.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A operação de cópia foi bem-sucedida em geral, mas uma ou mais entradas não puderam ser copiadas. Quando esse valor é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse valor, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IABContainer::CopyEntries** copia entradas do mesmo contêiner ou de um contêiner diferente. Uma chamada para **CopyEntries** é funcionalmente equivalente a fazer as seguintes chamadas para cada entrada a ser copiada: 
  
1. O [método IABContainer::CreateEntry](iabcontainer-createentry.md) para criar a nova entrada. 
    
2. O [método IMAPIProp::GetProps](imapiprop-getprops.md) para ler as propriedades da entrada a ser copiada. 
    
3. O [método IMAPIProp::SetProps](imapiprop-setprops.md) para gravar propriedades na nova entrada. 
    
4. O método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova entrada para executar um salvar. 
    
5. O método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) da nova entrada para liberar a referência do contêiner. 
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Todos os contêineres que suportam o **método IABContainer::CopyEntries** devem ser modificáveis. Defina o sinalizador de AB_MODIFIABLE contêiner em sua **propriedade PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que ele é modificável. 
  
Você deve dar suporte a todos os sinalizadores; No entanto, a interpretação e o uso desses sinalizadores são específicos da implementação— ou seja, você pode determinar o que significa a semântica dos sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT no contexto de sua implementação. Se você não puder ou não determinar se uma entrada é duplicada, sempre permita que a entrada seja copiada. 
  
Se o CREATE_REPLACE sinalizador estiver definido, copie sempre a entrada independentemente de CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT estiver definida e se a entrada é uma duplicata. 
  
Se CREATE_REPLACE não estiver definido e CREATE_CHECK_DUP_STRICT estiver definido, verifique se há duplicatas. Se uma entrada for determinada como uma duplicata, não copie a entrada. 
  
Você não precisa dar suporte a CREATE_REPLACE; não oferecer CREATE_REPLACE significa que você pode ignorá-la com segurança e sempre executar uma cópia. 
  
Retornar o aviso MAPI_W_PARTIAL_COMPLETION somente se uma entrada sem duplicação não puder ser copiada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use os sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT para indicar ao provedor como você deseja que o contêiner execute a verificação de entrada duplicada. Se você precisar ter uma entrada adicionada independentemente de ser uma duplicata, não de definir nenhum desses sinalizadores ou de definir o sinalizador CREATE_REPLACE aplicativo. CREATE_REPLACE indica que você não se importa se uma entrada for duplicada; você sempre quer que ele substitua a entrada original. 
  
## <a name="see-also"></a>Confira também



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


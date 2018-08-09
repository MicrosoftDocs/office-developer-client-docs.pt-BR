---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 304295e3ac77fb67ec5875620a7a269377b542c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767150"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Aplica-se a**: Outlook 
  
Atualiza uma ou mais propriedades.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _cValues_
  
> [in] A contagem dos valores de propriedade apontado pelo parâmetro _lpPropArray_ . O parâmetro _cValues_ não deve ser de 0. 
    
 _lpPropArray_
  
> [in] Um ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) que contêm valores de propriedade a ser atualizado. 
    
 _lppProblems_
  
> [além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, NULL, indicando sem a necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **SetProps** retorna informações detalhadas sobre erros na atualização de uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As propriedades foram atualizadas com êxito.
    
Os seguintes valores podem ser retornados na estrutura de **SPropProblemArray** , mas não como valores de retorno para **SetProps**:
  
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser atualizada porque ele é somente leitura, computado pelo provedor de serviços que é responsável pelo objeto.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para modificar um objeto somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> A propriedade não pode ser atualizada porque ela é maior que o tamanho do buffer do procedimento remoto (RPC) da chamada.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pela implementação de chamada.
    
## <a name="notes-to-implementers"></a>Notas para implementadores

Ignore a marca de propriedade **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) e todas as propriedades com um tipo de **PT_ERROR**. Não faça alterações ou relatar problemas na estrutura de **SPropProblemArray** . 
  
Retorne MAPI_E_INVALID_PARAMETER se uma propriedade do tipo **PT_OBJECT** é incluída na matriz de valores de propriedade. Também retorne esse erro se uma propriedade de valores múltiplos é incluída na matriz e sua lista de membros **cValues** estiver definido como 0. 
  
Se a chamada tiver êxito geral, mas há problemas com a definição de algumas das propriedades, volte S_OK e coloque as informações sobre os problemas na entrada da estrutura **SPropProblemArray** que o parâmetro _lppProblems_ aponta para. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Dependendo do provedor de serviço, você também poderá alterar o tipo de propriedade passando-se uma marca de propriedade que contém um tipo diferente que foi usado anteriormente com um identificador de propriedade fornecida.
  
Se você incluir uma marca de propriedade para uma propriedade que não é suportada pelo objeto e a implementação do **SetProps** permite a criação de novas propriedades, a propriedade é adicionada ao objeto. Qualquer valor anterior armazenado com o identificador de propriedade que foi usado para a nova propriedade é desconsiderado. 
  
Observe que o valor de retorno S_OK não garante que todas as propriedades foram atualizadas com êxito. Alguns provedores de cache **SetProps** chamadas até que recebam uma chamada que requer intervenção do provedor, como [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md). Portanto, é possível receber valores de erro que se relacionam com a chamada de **SetProps** com as chamadas posteriores. 
  
Se **SetProps** Retorna S_OK, verifique a estrutura de **SPropProblemArray** apontada pela _lppProblems_ para problemas na atualização propriedades individuais. Se **SetProps** retornará um erro, não marque a matriz de problema de propriedade. Em vez disso, chame o método do objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . 
  
Ao atualizar as propriedades grandes, **SetProps** pode falhar e retornar MAPI_E_NOT_ENOUGH_MEMORY. Não há nenhum tamanho máximo para propriedades e objetos de diferentes podem ter diferentes limites. Se você lida com as propriedades potencialmente grandes, prepare-se para chamar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com IID_IStream como o identificador de interface se **SetProps** retornar esse valor de erro. 
  
Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a estrutura **SPropProblemArray** . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI usa o método **IMAPIProp::SetProps** para gravar uma propriedade de volta a um objeto após a propriedade ter sido editada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


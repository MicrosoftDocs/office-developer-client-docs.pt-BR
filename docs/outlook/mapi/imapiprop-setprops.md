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
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412615"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] A contagem de valores de propriedade apontados pelo _parâmetro lpPropArray._ O  _parâmetro cValues_ não deve ser 0. 
    
 _lpPropArray_
  
> [in] Um ponteiro para uma matriz de [estruturas SPropValue](spropvalue.md) que contêm valores de propriedade a serem atualizados. 
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro para um ponteiro para uma [estrutura SPropProblemArray;](spropproblemarray.md) caso contrário, NULL, indicando que não há necessidade de informações de erro. Se  _lppProblems_ for um ponteiro válido na entrada, **SetProps** retornará informações detalhadas sobre erros na atualização de uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram atualizadas com êxito.
    
Os seguintes valores podem ser retornados na **estrutura SPropProblemArray,** mas não como valores de retorno **para SetProps**:
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser atualizada porque é somente leitura, calculada pelo provedor de serviços responsável pelo objeto.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar um objeto somente leitura ou acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> A propriedade não pode ser atualizada porque é maior do que o tamanho do buffer de chamada de procedimento remoto (RPC).
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pela implementação da chamada.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Ignore a **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) e todas as propriedades com um tipo de **PT_ERROR**. Não faça alterações ou reporte problemas na **estrutura SPropProblemArray.** 
  
Retornar MAPI_E_INVALID_PARAMETER se uma propriedade do tipo **PT_OBJECT** for incluída na matriz de valores de propriedade. Também retornará esse erro se uma propriedade de vários valores estiver incluída na matriz e seu membro **cValues** estiver definido como 0. 
  
Se a chamada for bem-sucedida em geral, mas houver problemas com a definição de algumas das propriedades, retorne S_OK e coloque informações sobre os problemas na entrada apropriada da estrutura **SPropProblemArray** para a que o parâmetro  _lppProblems_ aponta. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Dependendo do provedor de serviços, você também pode alterar o tipo de propriedade passando uma marca de propriedade que contém um tipo diferente do usado anteriormente com um determinado identificador de propriedade.
  
Se você incluir uma marca de propriedade para uma propriedade sem suporte pelo objeto e a implementação de **SetProps** permitir a criação de novas propriedades, a propriedade será adicionada ao objeto. Qualquer valor anterior armazenado com o identificador de propriedade que foi usado para a nova propriedade é descartado. 
  
Observe que o S_OK de retorno não garante que todas as propriedades foram atualizadas com êxito. Alguns provedores armazenam em cache chamadas **SetProps** até receberem uma chamada que exija intervenção do provedor, como [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md). Portanto, é possível receber valores de erro relacionados à chamada **SetProps** com as chamadas posteriores. 
  
Se **SetProps** retornar S_OK, verifique a estrutura **SPropProblemArray** apontada por  _lppProblems_ para problemas de atualização de propriedades individuais. Se **SetProps** retornar um erro, não verifique a matriz do problema de propriedade. Em vez disso, chame o método [IMAPIProp::GetLastError do](imapiprop-getlasterror.md) objeto. 
  
Ao atualizar propriedades grandes, **SetProps** pode falhar e retornar MAPI_E_NOT_ENOUGH_MEMORY. Não há um tamanho máximo para propriedades, e objetos diferentes podem ter limites diferentes. Se você lidar com propriedades potencialmente grandes, esteja preparado para chamar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com IID_IStream como o identificador de interface se **SetProps** retornar esse valor de erro. 
  
Chame a [função MAPIFreeBuffer](mapifreebuffer.md) para liberar **a estrutura SPropProblemArray.** 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI usa o **método IMAPIProp::SetProps** para gravar uma propriedade de volta em um objeto após a propriedade ter sido editada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


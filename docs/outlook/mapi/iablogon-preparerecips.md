---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423857"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parâmetros

_ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o tipo de texto nas cadeias de caracteres retornadas. O sinalizador a seguir pode ser definido:
    
  - MAPI_CACHE_ONLY: use somente o livro de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
_lpPropTagArray_
  
> [in] Um ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades que exigem atualização, se alguma. O  _parâmetro lpPropTagArray_ pode ser NULL. 
    
_lpRecipList_
  
> [in] Um ponteiro para uma [estrutura ADRLIST](adrlist.md) que contém a lista de destinatários. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A lista de destinatários foi preparada com êxito.
    
MAPI_E_NOT_FOUND 
  
> Um ou mais dos destinatários no parâmetro  _lpRecipList_ não existem. 
    
## <a name="return-value"></a>Valor de retorno

Um cliente chama o método [MAPI IAddrBook::P repareRecips](iaddrbook-preparerecips.md) para modificar ou reorganizar um conjunto de propriedades para um ou mais destinatários. Os destinatários podem ou não fazer parte da lista de destinatários de uma mensagem de saída. MAPI transfers this call to an address book provider's **IABLogon::P repareRecips** method. 
  
**IABLogon::P repareRecips** executa quatro tarefas principais: 
  
- Garante que todos os destinatários na lista de endereços apontados pelo parâmetro  _lpRecipList_ tenham um identificador de entrada de longo prazo. 
    
- Garante que todos os destinatários tenham as propriedades especificadas na matriz de valores de propriedade apontada pelo _parâmetro lpPropTagArray._ 
    
- Garante que as propriedades da matriz de valores de propriedade apareçam antes de quaisquer outras propriedades que existiam antes da chamada.
    
- Garante que a ordem das propriedades na estrutura [ADRENTRY](adrentry.md) de cada destinatário na estrutura **ADRLIST** seja a mesma da matriz de valores da propriedade. 
    
A **estrutura ADRENTRY** no  _parâmetro lpRecipList_ contém uma **estrutura ADRENTRY** para cada destinatário. Cada **estrutura ADRENTRY** contém uma matriz [de estruturas SPropValue](spropvalue.md) para descrever as propriedades do destinatário. Quando **IABLogon::P repareRecips** retorna, a matriz de estrutura **SPropValue** para cada destinatário inclui as propriedades do  _lpPropTagArray_ seguidas pelas outras propriedades do destinatário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Implementar **IABLogon::P repareRecips** envolve colocar propriedades em uma ordem específica, recuperar valores de propriedade e converter identificadores de entrada de curto prazo em identificadores de entrada de longo prazo. As propriedades solicitadas no parâmetro _lpPropTagArray_ devem estar no início da matriz de valores de propriedade associada à estrutura **ADRENTRY** de cada destinatário no parâmetro _lpRecipList._ Se os valores dessas propriedades não existirem, abra o usuário de mensagens associado ou a lista de distribuição usando seu identificador de entrada e recupere os valores de propriedade ausentes. 
  
Aloce **cada estrutura SPropValue** passada  _em lpRecipList_ separadamente para que as estruturas possam ser liberadas individualmente. Se você precisa alocar espaço adicional para qualquer estrutura **SPropValue,** por exemplo, para armazenar os dados de uma propriedade de cadeia de caracteres, use a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar espaço adicional para a matriz de valores de propriedade completa. Use a [função MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de valores de propriedade original e, em seguida, use a função [MAPIAllocateMore](mapiallocatemore.md) para alocar qualquer memória adicional necessária. 
  
Para implementar **IABLogon::P repareRecips,** use o procedimento a seguir:
  
1. Verifique se há entradas no _parâmetro lpPropTagArray._ Se a matriz de valores da propriedade estiver vazia, não há trabalho a ser fazer. Retornar um valor de sucesso. 
    
2. Processe cada destinatário no _parâmetro lpRecipList._ Há um membro **de estrutura ADRENTRY** para cada destinatário na lista. Ignore os seguintes tipos de destinatários: 
    
   - Destinatários sem um identificador de entrada **no membro rgPropVals** de sua estrutura **ADRENTRY** (ou seja, destinatários não resolvidos). 
    
   - Destinatários com um identificador de entrada que não pertence ao seu provedor. Esses destinatários serão passados para outro provedor de agendas.
    
3. Abra o destinatário e recupere as propriedades que já estão definidas para o destinatário.
    
4. Mesclar a matriz de valores de propriedade especificada no  _lpRecipList_ com a matriz de propriedades retornadas de **GetProps**. Se a mesma propriedade ocorrer em ambas as matrizes de propriedades, use o valor de  _lpRecipList_.
    
5. Se a  _matriz de valores da propriedade lpRecipList_ for grande o suficiente para manter todas as propriedades necessárias, basta substituí-la pela matriz mesclada. Se a  _matriz de valores da propriedade lpRecipList_ não for grande o suficiente, substitua-a por uma matriz recém-alocada. Certifique-se de que a nova matriz tenha um valor atualizado em cada um de seus **membros cValues.** 
    
6. Se você não reconhecer uma ou mais das propriedades no parâmetro  _lpPropTagArray,_ de definir o tipo de propriedade na estrutura **ADRENTRY** do destinatário como PT_ERROR e o valor da propriedade como MAPI_E_NOT_FOUND ou com outro valor que dê um motivo mais específico para a indisponibilidade da propriedade. Para obter informações sobre PT_ERROR, consulte [Tipos de Propriedade.](property-types.md)
    
> [!NOTE]
> Nunca realoque a estrutura **ADRLIST** que é passada para **IABLogon::P repareRecips** ou altere seu número de entradas. 
  
## <a name="see-also"></a>Confira também

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)


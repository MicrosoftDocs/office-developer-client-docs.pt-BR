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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348941"
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
  
> no Uma bitmask de sinalizadores que controla o tipo de texto nas cadeias de caracteres retornadas. O seguinte sinalizador pode ser definido:
    
  - MAPI_CACHE_ONLY: Use apenas o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
_lpPropTagArray_
  
> no Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades que precisam ser atualizadas, se houver. O parâmetro _lpPropTagArray_ pode ser NULL. 
    
_lpRecipList_
  
> no Um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que contém a lista de destinatários. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A lista de destinatários foi preparada com êxito.
    
MAPI_E_NOT_FOUND 
  
> Um ou mais dos destinatários no parâmetro _lpRecipList_ não existem. 
    
## <a name="return-value"></a>Valor de retorno

Um cliente chama o método MAPI [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) para modificar ou reorganizar um conjunto de propriedades para um ou mais destinatários. Os destinatários podem ou não fazer parte da lista de destinatários de uma mensagem de saída. MAPI transfere essa chamada para um provedor de catálogo de endereços **IABLogon: método reparerecips do:P** . 
  
**IABLogon::P reparerecips** executa quatro tarefas principais: 
  
- Garante que todos os destinatários na lista de endereços apontados pelo parâmetro _lpRecipList_ tenham um identificador de entrada de longo prazo. 
    
- Garante que todos os destinatários tenham as propriedades especificadas na matriz de valor da propriedade apontada pelo parâmetro _lpPropTagArray_ . 
    
- Garante que as propriedades da matriz de valor da propriedade apareçam antes de qualquer outra propriedade que existia antes da chamada.
    
- Garante que a ordem das propriedades na estrutura [ADRENTRY](adrentry.md) de cada destinatário na estrutura **das ADRLIST** seja igual à da matriz de valor da propriedade. 
    
A estrutura **ADRENTRY** no parâmetro _lpRecipList_ contém uma estrutura **ADRENTRY** para cada destinatário. Cada estrutura **ADRENTRY** contém uma matriz de estruturas [SPropValue](spropvalue.md) para descrever as propriedades do destinatário. Quando **IABLogon::P reparerecips** retorna, a matriz de estrutura **SPropValue** para cada destinatário inclui as propriedades do _lpPropTagArray_ seguidas pelas outras propriedades do destinatário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Implementando **IABLogon::P reparerecips** envolve a colocação de propriedades em uma ordem específica, recuperação de valores de propriedade e conversão de identificadores de entrada de curto prazo para identificadores de entrada de longo prazo. As propriedades que são solicitadas no parâmetro _lpPropTagArray_ devem estar no início da matriz de valor da propriedade associada à estrutura **ADRENTRY** de cada destinatário no parâmetro _lpRecipList_ . Se não houver valores para essas propriedades, abra o usuário de mensagens associado ou a lista de distribuição usando seu identificador de entrada e recupere os valores de propriedade ausentes. 
  
Alocar cada estrutura **SPropValue** passada no _lpRecipList_ separadamente para que as estruturas possam ser liberadas individualmente. Se você precisar alocar espaço adicional para qualquer estrutura do **SPropValue** , por exemplo, para armazenar os dados de uma propriedade de cadeia de caracteres, use a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar espaço adicional para a matriz de valor de propriedade completa. Use a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de valor da propriedade original e, em seguida, use a função [MAPIAllocateMore](mapiallocatemore.md) para alocar qualquer memória adicional necessária. 
  
Para implementar o **IABLogon::P reparerecips**, use o seguinte procedimento:
  
1. Verifique as entradas no parâmetro _lpPropTagArray_ . Se a matriz de valor da propriedade estiver vazia, não haverá trabalho pendente. Retornar um valor de sucesso. 
    
2. Processe cada destinatário no parâmetro _lpRecipList_ . Há um membro da estrutura **ADRENTRY** para cada destinatário na lista. Ignore os seguintes tipos de destinatários: 
    
   - Destinatários sem um identificador de entrada no membro **rgPropVals** da estrutura do **ADRENTRY** (ou seja, destinatários não resolvidos). 
    
   - Destinatários com um identificador de entrada que não pertence ao provedor. Esses destinatários serão passados para outro provedor de catálogo de endereços.
    
3. Abra o destinatário e recupere as propriedades já definidas para o destinatário.
    
4. Mescle a matriz de valor de propriedade especificada no _lpRecipList_ com a matriz de propriedades retornada **** de GetProps. Se a mesma propriedade ocorrer em ambas as matrizes de propriedade, use o valor de _lpRecipList_.
    
5. Se a matriz de valor da propriedade _lpRecipList_ for grande o suficiente para manter todas as propriedades necessárias, basta substituí-la pela matriz mesclada. Se a matriz de valor da propriedade _lpRecipList_ não for grande o suficiente, substitua-a por uma matriz alocada recentemente. Certifique-se de que a nova matriz tem um valor atualizado em cada um dos seus membros do **cValues** . 
    
6. Se você não reconhecer uma ou mais propriedades no parâmetro _lpPropTagArray_ , defina o tipo de propriedade na estrutura **ADRENTRY** do destinatário como PT_ERROR e o valor da propriedade como MAPI_E_NOT_FOUND ou como outro valor que forneça mais motivo específico para a indisponibilidade da propriedade. Para obter informações sobre o PT_ERROR, consulte [tipos de propriedade](property-types.md).
    
> [!NOTE]
> Nunca realoque a estrutura **das ADRLIST** que é passada para **IABLogon::P reparerecips** ou alterar seu número de entradas. 
  
## <a name="see-also"></a>Confira também

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)


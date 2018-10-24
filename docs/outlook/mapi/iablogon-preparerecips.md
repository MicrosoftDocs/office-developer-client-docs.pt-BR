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
ms.openlocfilehash: c42077528a4f7227321d8f987cc5dd0ccd4c966c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589739"
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
  
> [in] Uma bitmask dos sinalizadores que controla o tipo do texto em cadeias de caracteres retornadas. O seguinte sinalizador pode ser definido:
    
  - MAPI_CACHE_ONLY: Use somente o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
_lpPropTagArray_
  
> [in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades que requeiram a atualização, se houver alguma. O parâmetro _lpPropTagArray_ pode ser NULL. 
    
_lpRecipList_
  
> [in] Um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém a lista de destinatários. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A lista de destinatários foi preparada com êxito.
    
E_NOT_FOUND 
  
> Um ou mais dos destinatários no parâmetro _lpRecipList_ não existem. 
    
## <a name="return-value"></a>Valor de retorno

Um cliente chama o método MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) para modificar ou reorganizar um conjunto de propriedades para um ou mais destinatários. Os destinatários podem ou não podem ser a parte da lista de destinatários de uma mensagem de saída. MAPI transfere essa chamada para o método de **IABLogon::PrepareRecips** de um provedor catálogo de endereços. 
  
**IABLogon::PrepareRecips** executa as quatro tarefas principais: 
  
- Garante que todos os destinatários na lista de endereços apontadas pelo parâmetro _lpRecipList_ tiver um identificador de entrada de longo prazo. 
    
- Garante que todos os destinatários tenham as propriedades especificadas na matriz de valores de propriedade apontado pelo parâmetro _lpPropTagArray_ . 
    
- Garante que as propriedades da matriz de valores de propriedade aparecem antes de quaisquer outras propriedades que se encontrava antes da chamada.
    
- Garante que a ordem das propriedades na estrutura [ADRENTRY](adrentry.md) de cada destinatário na estrutura de **ADRLIST** é o mesmo que a matriz de valores de propriedade. 
    
A estrutura **ADRENTRY** no parâmetro _lpRecipList_ contém uma estrutura **ADRENTRY** para cada destinatário. Cada estrutura **ADRENTRY** contém uma matriz de estruturas [SPropValue](spropvalue.md) para descrever as propriedades do destinatário. Quando **IABLogon::PrepareRecips** retorna, a matriz de estrutura de **SPropValue** para cada destinatário inclui as propriedades de _lpPropTagArray_ seguido as outras propriedades para o destinatário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Implementar **IABLogon::PrepareRecips** envolve a colocação de propriedades em uma ordem específica, recuperando valores de propriedade e conversão de curto prazo identificadores de entrada aos identificadores de entrada de longo prazo. As propriedades que são solicitadas no parâmetro _lpPropTagArray_ devem ser no início da matriz de valores de propriedade associado a estrutura **ADRENTRY** de cada destinatário no parâmetro _lpRecipList_ . Se os valores dessas propriedades não existirem, abra a lista de distribuição ou usuário mensagens associada usando seu identificador de entrada e recuperar os valores de propriedade ausente. 
  
Aloca cada estrutura **SPropValue** passada na _lpRecipList_ separadamente para que as estruturas podem ser liberadas individualmente. Se você deve alocar espaço adicional para qualquer estrutura **SPropValue** , por exemplo, para armazenar os dados para uma propriedade de cadeia de caracteres, use a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar espaço adicional para a matriz de valor de propriedade completo. Use a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de valores de propriedade original e, em seguida, use a função de [MAPIAllocateMore](mapiallocatemore.md) para alocar toda a memória adicional que é necessária. 
  
Para implementar **IABLogon::PrepareRecips**, use o procedimento a seguir:
  
1. Verifique se há entradas no parâmetro _lpPropTagArray_ . Se a matriz de valores de propriedade estiver vazia, não há nenhum trabalho a ser feito. Retorna um valor de sucesso. 
    
2. Processo de cada destinatário no parâmetro _lpRecipList_ . Não há um membro de estrutura **ADRENTRY** para cada destinatário na lista. Ignore os seguintes tipos de destinatários: 
    
   - Destinatários sem um identificador de entrada no membro **rgPropVals** da sua estrutura **ADRENTRY** (ou seja, os destinatários não resolvidos). 
    
   - Destinatários com um identificador de entrada que não pertencem ao provedor. Esses destinatários serão transmitidos ao outro provedor de catálogo de endereços.
    
3. Abra o destinatário e recuperar as propriedades que já estão definidas para o destinatário.
    
4. Mescle a matriz de valores de propriedade especificado no _lpRecipList_ com a matriz de propriedades retornado da **GetProps**. Se a mesma propriedade ocorre em ambas as matrizes de propriedade, use o valor de _lpRecipList_.
    
5. Se a matriz de valores de propriedade _lpRecipList_ é grande o suficiente para armazenar todas as propriedades necessárias, simplesmente substitua-la com a matriz mesclada. Se a matriz de valor de propriedade _lpRecipList_ não é grande o suficiente, substitua-o com uma matriz alocada recentemente. Certifique-se de que a nova matriz tem um valor atualizado em cada um dos seus membros **cValues** . 
    
6. Se você não reconhecer uma ou mais das propriedades no parâmetro _lpPropTagArray_ , definir o tipo de propriedade na estrutura **ADRENTRY** do destinatário PT_ERROR e o valor da propriedade para E_NOT_FOUND ou para outro valor que oferece uma mais motivo específico de indisponibilidade da propriedade. Para obter informações sobre PT_ERROR, consulte [Tipos de propriedade](property-types.md).
    
> [!NOTE]
> Nunca realocar a estrutura **ADRLIST** que é passada para **IABLogon::PrepareRecips** ou alterar seu número de entradas. 
  
## <a name="see-also"></a>Confira também

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propriedade canônico PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)


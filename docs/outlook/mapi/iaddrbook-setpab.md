---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424613"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Designa um contêiner específico como o pab (lista de endereços pessoal).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do contêiner a ser designado como o PAB. O  _parâmetro lpEntryID_ não pode ser NULL. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O contêiner especificado foi estabelecido como o PAB.
    
## <a name="remarks"></a>Comentários

Os clientes e provedores de serviços chamam **o método SetPAB** para designar um contêiner específico como a PAB. A PAB é um contêiner que consiste em entradas copiadas de outros contêineres, bem como novas entradas. 
  
Uma chamada para **SetPAB** estabelece um contêiner como o PAB até que esse contêiner se torne indisponível ou um novo contêiner se torne o PAB por meio de uma chamada subsequente para **SetPAB**. 
  
Os clientes e provedores não têm que chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para tornar a alteração de PAB permanente. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI usa o **método SetPAB** para tornar o contêiner especificado o PAB.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriedade canônica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)


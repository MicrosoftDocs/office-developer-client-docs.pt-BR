---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347800"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um fluxo XML que representa as informações recuperadas do serviço de descoberta automática de um servidor microsoft Exchange 2007.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |olmapi32.dll  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Parâmetros

 _pwzAddress_
  
> [in] Um endereço de email SMTP (Simple Mail Transfer Protocol) encerrado por nulo da conta para a qual você deseja recuperar as informações de descoberta automática.
    
 _pwzPassword_
  
> [in] Uma senha opcional para a conta especificada por  _pwzAddress_. Observe que passar qualquer senha não terá efeito se a conta especificada por  _pwzAddress_ não exigir uma senha. 
    
 _hCancelEvent_
  
> [in] Uma alça de evento Win32 não configurada que é opcional e pode ser usada para cancelar a operação. Para cancelar a operação, de definir o evento e passar o alça de evento como  _hCancelEvent_; passe **nulo** se não quiser cancelar a operação. Observe que passar um valor que não representa uma alça de evento não tem efeito e é ignorado pela função. 
    
 _ulFlags_
  
> [in] Este parâmetro não é usado. Deve ser 0.
    
 _ppXmlStream_
  
> [out] Um ponteiro para um [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que contém o XML de descoberta automática. Retorna **nulo** se a operação de descoberta automática falhar. Você deve liberar o [objeto IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) quando terminar. 
    
## <a name="return-values"></a>Valor de retorno

S_OK 
  
- A chamada de função é bem-sucedida.
    
E_INVALIDARG 
  
-  _pwzAddress_ é **nulo** ou não é um endereço SMTP válido ou _ppXmlStream_ é um ponteiro **nulo** para [um objeto IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
MAPI_E_NOT_FOUND 
  
- O computador cliente não está conectado à rede, o computador cliente não está conectado a um servidor do Microsoft Exchange 2007, o  _pwzAddress_ não é uma conta em um servidor Exchange 2007 ou  _o pwzAddress_ é uma conta que não dá suporte ao serviço de descoberta automática do Exchange. 
    
MAPI_E_USER_CANCEL 
  
- Uma alça de evento foi passada para  _hCancelEvent_ para cancelar a operação. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- O valor passado para  _pwzAddress_ ou  _pwzPassword_ é muito longo, de forma que ele ultrapasse o buffer interno de tamanho de 256 bytes. 
    


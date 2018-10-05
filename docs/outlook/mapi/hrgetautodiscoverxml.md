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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400716"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um fluxo de Extensible Markup Language (XML) que representa as informações recuperadas do serviço de descoberta automática de um servidor Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |olmapi32.dll  <br/> |
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
  
> [in] Um terminada em nulo Simple Mail Transfer Protocol (SMTP) endereço de email da conta para o qual você deseja recuperar as informações de descoberta automática.
    
 _pwzPassword_
  
> [in] Uma senha opcional para a conta especificada pelo _pwzAddress_. Observe que passar qualquer senha não tem efeito se a conta especificada pelo _pwzAddress_ não exigir uma senha. 
    
 _hCancelEvent_
  
> [in] Um não definido identificador de eventos de Win32 que é opcional e pode ser usado para cancelar a operação. Para cancelar a operação, defina o evento e passar o identificador de eventos como _hCancelEvent_; passe **null** se não desejar cancelar a operação. Observação passando um valor que não representam um identificador de eventos não tem efeito e é ignorada pela função. 
    
 _ulFlags_
  
> [in] Este parâmetro não é usado. Ela deve ser 0.
    
 _ppXmlStream_
  
> [out] Um ponteiro para um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que contém a XML de descoberta automática. Retorna **null** se a operação de descoberta automática falhar. Você deve liberar o objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) quando terminar com ele. 
    
## <a name="return-values"></a>Valores de retorno

S_OK 
  
- A chamada de função é bem-sucedida.
    
E_INVALIDARG 
  
-  _pwzAddress_ é **Nulo** ou não é um endereço SMTP válido, ou _ppXmlStream_ é um ponteiro **Nulo** para um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
    
E_NOT_FOUND 
  
- Computador cliente não está conectado à rede, computador cliente não está conectado a um servidor Microsoft Exchange 2007, _pwzAddress_ não for uma conta em um servidor Exchange 2007 ou _pwzAddress_ é uma conta que não oferece suporte para Exchange serviço de descoberta automática. 
    
MAPI_E_USER_CANCEL 
  
- Um identificador de eventos foi passado para _hCancelEvent_ para cancelar a operação. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- O valor passado para _pwzAddress_ ou _pwzPassword_ é muito longo, de forma que ele estouros de buffer interno do tamanho de 256 bytes. 
    


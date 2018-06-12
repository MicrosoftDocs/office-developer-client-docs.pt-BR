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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: da466fc9add8cbc385014782f31749d3b6522da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766781"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Aplica-se a**: Outlook 
  
Retorna um fluxo de Extensible Markup Language (XML) que representa as informações recuperadas do serviço de descoberta automática de um servidor Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |olmapi32.dll  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Par�metros

 _pwzAddress_
  
> [in] Um terminada em nulo Simple Mail Transfer Protocol (SMTP) endereço de email da conta para o qual você deseja recuperar as informações de descoberta automática.
    
 _pwzPassword_
  
> [in] Uma senha opcional para a conta especificada pelo _pwzAddress_. Observe que passar qualquer senha não tem efeito se a conta especificada pelo _pwzAddress_ não exigir uma senha. 
    
 _hCancelEvent_
  
> [in] Um não definido identificador de eventos de Win32 que é opcional e pode ser usado para cancelar a operação. Para cancelar a operação, defina o evento e passar o identificador de eventos como _hCancelEvent_; passe **null** se não desejar cancelar a operação. Observação passando um valor que não representam um identificador de eventos não tem efeito e é ignorada pela função. 
    
 _ulFlags_
  
> [in] Este parâmetro não é usado. Ela deve ser 0.
    
 _ppXmlStream_
  
> [out] Um ponteiro para um objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) que contém a XML de descoberta automática. Retorna **null** se a operação de descoberta automática falhar. Você deve liberar o objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) quando terminar com ele. 
    
## <a name="return-values"></a>Valores de retorno

S_OK 
  
- A chamada de função é bem-sucedida.
    
E_INVALIDARG 
  
-  _pwzAddress_ é **Nulo** ou não é um endereço SMTP válido, ou _ppXmlStream_ é um ponteiro **Nulo** para um objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
    
E_NOT_FOUND 
  
- Computador cliente não está conectado à rede, computador cliente não está conectado a um servidor Microsoft Exchange 2007, _pwzAddress_ não for uma conta em um servidor Exchange 2007 ou _pwzAddress_ é uma conta que não oferece suporte para Exchange serviço de descoberta automática. 
    
MAPI_E_USER_CANCEL 
  
- Um identificador de eventos foi passado para _hCancelEvent_ para cancelar a operação. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- O valor passado para _pwzAddress_ ou _pwzPassword_ é muito longo, de forma que ele estouros de buffer interno do tamanho de 256 bytes. 
    


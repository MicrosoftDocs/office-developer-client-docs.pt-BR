---
title: Criar um controle ActiveX que pode vincular dados de formulário do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Você pode hospedar controles ActiveX em formulários do InfoPath que foram projetados para ser aberto no editor do InfoPath. Esses controles podem ser preexistente (com algumas restrições) ou podem ser escritos especificamente para o InfoPath.
ms.openlocfilehash: 90378533a7c3cde4a1927753c0325fdd8d0b3ce5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765594"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a>Criar um controle ActiveX que pode vincular dados de formulário do InfoPath

Você pode hospedar controles ActiveX em formulários do InfoPath que foram projetados para ser aberto no editor do InfoPath. Esses controles podem ser preexistente (com algumas restrições) ou podem ser escritos especificamente para o InfoPath.
  
## <a name="write-an-activex-control"></a>Escrever um controle ActiveX

Assim como acontece com outros controles no InfoPath, os controles ActiveX devem oferecer suporte a interfaces existentes do objeto COM (Component Model):
  
- **IDispatch**
    
- **IPersistPropertyBag**
    
- **IPersistStreamInit**
    
- **IPropertyPage**
    
- **IObjectSafety**
    
- **IPropertyNotifySink**
    
- **IViewObject**
    
- **IOleObject**
    
- **IOleInPlaceObject**
    
Na ordem do InfoPath atualizar as propriedades no documento DOM (Object Model) no momento em que eles alterar no controle, o controle deve implementar estas interfaces:
  
- **IConnectionPointContainer**
    
- **IEnumConnectionPoints**
    
- **IConnectionPoint**
    
- **IEnumConnections**
    
Além disso, há duas interfaces COM InfoPath específica que oferecem maior integração dos controles:
  
- [IInfoPathControl](http://msdn.microsoft.com/en-us/library/bb264625.aspx)
    
- [IInfoPathControlSite](http://msdn.microsoft.com/en-us/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a>Adicionar um controle ActiveX para o ambiente de Design do InfoPath

O comando **Adicionar ou remover controles personalizados** no painel de tarefas **controles** permite que você use o **Assistente para adicionar personalizado controle** para adicionar um controle personalizado. Usando o assistente, você pode selecionar um controle ActiveX que já foi registrado ou localizar controles personalizados adicionais no Office Marketplace. Depois de selecionar um controle, você pode especificar os itens a seguir. 
  
- Especifique um arquivo CAB para instalar o controle ActiveX com o seu modelo de formulário.
    
- Especifique uma propriedade de vinculação para vincular ao XML.
    
- Especifique uma propriedade que é usada para habilitar ou desabilitar o controle em resposta às regras ou assinaturas digitais, que podem ser útil, por exemplo, quando o XML não estiver presente ou quando a formatação condicional é usada.
    
- Especificar dados digite ligação.
    
> [!NOTE]
> Se você estiver desenvolvendo um controle ActiveX e adicionou ao painel de tarefas **controles** no InfoPath, não será possível reconstruir o controle ActiveX até InfoPath é fechado. 
  
## <a name="deploy-an-activex-control"></a>Implantar um controle ActiveX

Para distribuir um controle ActiveX, você pode escrever um instalador que instala o controle no computador de destino e copia o arquivo de modelo de controle do InfoPath (ICT) e o arquivo CAB para a pasta do usuário, \Users\\< username\>\AppData\Local\ Microsoft\InfoPath\Controls. Observe que se dois ou mais desenvolvedores estão colaborando sobre como desenvolver formulários que usam os controles ActiveX, cada desenvolvedor deve ter os controles que foram adicionados ao ambiente de design do InfoPath ou não será possível modificar as propriedades dos controles do InfoPath.
  
## <a name="see-also"></a>Confira também



Laboratório 6: Adicionando controles ActiveX no InfoPath 2003
  
[Criar um controle personalizado do InfoPath usando c# e .NET (Blog da equipe do InfoPath)](http://blogs.msdn.com/infopath/archive/2005/04/15/creating-an-infopath-custom-control-using-c-and-net.aspx)


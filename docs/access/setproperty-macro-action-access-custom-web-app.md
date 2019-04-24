---
title: Ação de macro SetProperty (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Você pode usar a ação setProperty para definir uma propriedade para um controle em um modo de exibição.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307886"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>Ação de macro SetProperty (aplicativo Web personalizado do Access)

Você pode usar a **** ação setProperty para definir uma propriedade para um controle em um modo de exibição. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A **** ação setProperty tem os argumentos listados na tabela a seguir. 
  
|**Argumento da ação**|**Descrição**|
|:-----|:-----|
| _Nome do Controle_ <br/> |Digite o nome do campo ou do controle para o qual você deseja definir o valor da propriedade. Deixe este argumento em branco para definir a propriedade para o modo de exibição.  <br/> |
| _Property_ <br/> |Selecione a propriedade a ser definida. Consulte a seção **Comentários** deste artigo para obter uma lista das propriedades que podem ser definidas com esta ação.<br/> |
| _Valor_ <br/> |Digite o valor com o qual a propriedade deve ser definida. Para propriedades cujos valores sejam Sim ou Não, use **-1** para Sim e **0** para Não.<br/> |
   
## <a name="remarks"></a>Comentários

Você pode usar a **** ação setProperty para definir as seguintes propriedades de um controle: 
  
- Legenda
    
- Habilitado
    
- ForeColor
    
- Valor
    
- Visível
    
Se você inserir um valor inválido para o argumento ** *Valor* **, não ocorrerá nenhum erro, mas o Access poderá alterar a propriedade para um valor diferente, dependendo da forma como o Access interpretar o argumento. 
  


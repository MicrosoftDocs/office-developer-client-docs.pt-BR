---
title: Ação de Macro DefinirPropriedade (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Você pode usar a ação DefinirPropriedade para definir uma propriedade para um controle em um modo de exibição.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765221"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>Ação de Macro DefinirPropriedade (aplicativo da web personalizado do Access)

Você pode usar a ação **DefinirPropriedade** para definir uma propriedade para um controle em um modo de exibição. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **DefinirPropriedade** tem os argumentos listados na tabela a seguir. 
  
|**Argumento da ação**|**Descrição**|
|:-----|:-----|
| _Nome do Controle_ <br/> |Digite o nome do campo ou controle para o qual você deseja definir o valor da propriedade. Deixe este argumento em branco para definir a propriedade no modo de exibição.  <br/> |
| _Propriedade_ <br/> |Selecione a propriedade a ser definida. Consulte a seção **Comentários** deste artigo para obter uma lista das propriedades que podem ser definidas com esta ação.<br/> |
| _Valor_ <br/> |Digite o valor com o qual a propriedade deve ser definida. Para propriedades cujos valores sejam Sim ou Não, use **-1** para Sim e **0** para Não.<br/> |
   
## <a name="remarks"></a>Comentários

Você pode usar a ação **DefinirPropriedade** para definir as seguintes propriedades de um controle: 
  
- Caption
    
- Habilitado
    
- ForeColor
    
- Value
    
- Visible
    
Se você inserir um valor inválido para o argumento ** *Valor* **, não ocorrerá nenhum erro, mas o Access poderá alterar a propriedade para um valor diferente, dependendo da forma como o Access interpretar o argumento. 
  


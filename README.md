# OpenFOAM_NaturalConvection

## 106_sherer

熱伝達率の出力設定

```system/heatTransferCoeff
heatTransferCoeff1
{
    // Mandatory entries (unmodifiable)
    type            heatTransferCoeff;
    libs            (fieldFunctionObjects);
    field           T;//<field>;
    patches         (ball);//(<patch1> <patch2> ... <patchN>);
    htcModel        fixedReferenceTemperature;//<htcModel>;
    //UInf            (0 0 0);
    //Cp              CpInf;
    //CpInf           1000;
    //rho             rhoInf;
    //rhoInf          1.2;
    TRef              293;

    // Optional (inherited) entries
    //result          <fieldResult>;
    region          region0;
    enabled         true;
    log             true;
    timeStart       0;
    timeEnd         10000;
    executeControl  timeStep;
    executeInterval 500;
    writeControl    timeStep;
    writeInterval   500;
}
```

![image](https://github.com/kamakiri1225/OpenFOAM_NaturalConvection/assets/36812492/525dfe05-8a32-4631-83c0-450bd400b9a6)

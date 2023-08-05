FUNCTION_BLOCK FactoryIO_Scene1

VAR_INPUT
  In_0: BOOL; // Pallet arrival sensor
  In_3: BOOL; // Pallet departure sensor
END_VAR

VAR_OUTPUT
  Out_1: BOOL; // Entry conveyer
END_VAR

VAR
  Pallet_on_entry: BOOL; // State of the entry conveyer
END_VAR

METHOD Run
  R_In_0(CLK := In_0); // Detect arrival of pallet
  F_In_3(CLK := In_3); // Detect departure of pallet

  IF R_In_0.Q THEN // When a pallet arrives
    Pallet_on_entry := TRUE; // Set Pallet_on_entry
  END_IF;

  IF F_In_3.Q THEN // When a pallet departs
    Pallet_on_entry := FALSE; // Reset Pallet_on_entry
  END_IF;

  Out_1 := Pallet_on_entry; // The current state of the conveyer defines Out_1
END_METHOD

END_FUNCTION_BLOCK

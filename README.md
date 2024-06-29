# Synchronous-FIFO

## Introduction
A First-In-First-Out queue known as a synchronous FIFO uses a single clock pulse for both data write and read operations. The read and write operations in synchronous FIFO are carried out at the same speed. Because synchronous FIFOs operate at high speeds, they are mostly utilized in high-speed systems. Because synchronous FIFOs use free running clocks, they are easier to operate at high speeds than asynchronous FIFOs, which need two separate clocks for read and write operations. Compared to the asynchronous FIFO, the synchronous FIFO is more sophisticated.

## Working
2) Write Operation: This operation entails writing or storing data in the FIFO memory until any flag conditions indicating that writing should cease are raised. The data to be written is provided at the DIN port, the write 'wr' is set high, and the data is written at the subsequent rising edge to complete the write operation.

2) Read Operation: This is the action taken when we wish to retrieve data from the FIFO memory until it indicates that there is no more data available for retrieval; this is known as the "empty condition." Empty flags are used to generate empty conditions. In order to read data, we must first make the read 'rd' high. Then, when the next rising edge comes, the data will be at DOUT.

## Pointers Used
1) Write Pointer: This pointer controls the write operation of the FIFO. It used to points to the FIFO memory location where the data will be written.

2) Read Operation: The read operation is controlled by the read pointer. It will be pointing the location from where next data is to be read.

## Flags Used
Synchronous FIFO provides us with few flags, to determine the status or to interrupt the operation of FIFO.

1) EMPTY flag: This flags is useful to avoid the case of the invalid request of read operation when the FIFO is already empty.

2) FULL flag: This flags is useful to avoid the case of the invalid request of write operation when the FIFO is already full.


# Part B — Channel and Propagation Model

## Goal

Model a 4x4 Rayleigh-fading MIMO wireless channel with additive white Gaussian noise (AWGN) and compare how spatial correlation affects the behaviour of spatial diversity and spatial multiplexing.

## Channel representation

The assignment represents the received signal using the MIMO relationship

`y = Hx + n`

where `y` is the received-signal vector, `H` is the 4x4 channel matrix, `x` is the transmitted-signal vector, and `n` is the AWGN vector. Rayleigh fading is used to represent multipath channel variation.

## Spatial correlation cases

Two spatial-correlation settings are compared:

- `rho = 0`: uncorrelated channel branches.
- `rho = 0.8`: highly correlated channel branches.

The report uses channel-power visualizations and a median channel-condition-number comparison to illustrate that stronger correlation can make the MIMO channel harder to separate reliably.

## Performance measures

The reported evaluation plots cover:

- **BER (Bit Error Rate):** fraction of transmitted bits detected incorrectly.
- **PER (Packet Error Rate):** fraction of frames/packets containing at least one bit error.
- **Outage probability:** fraction of simulated frames that exceed the selected BER target.
- **Useful throughput:** successfully delivered payload bits per channel use, using the assignment's stated accounting.

The figures compare spatial diversity and spatial multiplexing over an `Eb/N0` sweep from 0 to 20 dB in 2 dB steps, for the considered correlation settings.

## Interpretation

The submitted plots indicate that increased spatial correlation degrades the reliability of spatial multiplexing more noticeably than diversity. Under favourable, weakly correlated channel conditions, multiplexing provides higher useful throughput at larger `Eb/N0`; diversity is the stronger choice when reliability is the main requirement.

These are observations from the assignment's particular simulated setup. They should not be treated as measurements from physical hardware or as universal performance guarantees.

## Scope note

This repository contains only explanatory documentation and selected result images. The original MATLAB implementation is intentionally not included, so the simulation cannot be rerun from this repository alone.

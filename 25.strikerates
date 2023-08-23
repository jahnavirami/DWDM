# Given strike rates
strike_rates <- c(100, 70, 60, 90, 90)

# (a) Min-Max Normalization
min_max_norm <- function(x) {
  (x - min(x)) / (max(x) - min(x))
}
min_max_normalized <- min_max_norm(strike_rates)

# (b) Z-Score Normalization
z_score_norm <- function(x) {
  (x - mean(x)) / sd(x)
}
z_score_normalized <- z_score_norm(strike_rates)

# (c) Z-Score Normalization using Mean Absolute Deviation (MAD)
z_score_mad_norm <- function(x) {
  (x - mean(x)) / mad(x)
}
z_score_mad_normalized <- z_score_mad_norm(strike_rates)

# (d) Decimal Scaling Normalization
decimal_scale_norm <- function(x) {
  max_digit <- max(floor(log10(abs(x))) + 1)
  x / (10^max_digit)
}
decimal_scaled <- decimal_scale_norm(strike_rates)

# Print the results
print("Min-Max Normalized:")
print(min_max_normalized)

print("Z-Score Normalized:")
print(z_score_normalized)

print("Z-Score MAD Normalized:")
print(z_score_mad_normalized)

print("Decimal Scaled:")
print(decimal_scaled)